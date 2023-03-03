---
title: (PLC)アプリケーションログ
permalink: ja_rsys_log.html
sidebar: Install_A_S_ja
topnav: topnav_ja
---

アプリケーションログの中、特別なキーワードをリアルタイムで検出したい場合はどうすれば良いでしょうか。

例えば、次のようなアプリケーションログの中　__2020010100037__　キーワードをリアルタイムで検出する場合です。

## 1. 収集されるログ確認

<!-- [![image](/docs/images/Ins_G/rsyslog/1.png)](/docs/images/Ins_G/rsyslog/1.png){:target="_blank"} -->

<br />

## 2. conf設定(rsyslog使用)
- 80-application.conf → confファイル生成

`# vi /etc/rsyslog.d/80-application.conf`

<br />

## 3. confファイル生成例

- File = “ログパス”, Tag = “ログタグ”, Severity = “重大度”   
- ファイル名にワイルドカードを使用が必要な場合、__rsyslogバージョン8.25以上__　を使用する必要があります。
   
     #variables required for non-syslog log file forwarding – application log file
     #edit on your location

     input(type=”imfile”
     File=”/var/log/application.log”
     Tag=”application”
     Severity=”info”
     Facility=”local7″)

     ###### Creates a template for each log file in the Logentries UI
     ### logic to apply the relevant templates to the different log files

     if $programname == “application” then /var/log/plura/ceelog-127.0.0.1.log;CEETemplate
     :programname, isequal, “application” ~

<br />

### 3-1. PLURA V5 repoからダウンロード

`# wget https://repo.plura.io/v5/module/rsyslog/80-application.conf`

`# curl https://repo.plura.io/v5/module/rsyslog/80-application.conf -o /etc/rsyslog.d/80-application.conf`

<br />

## 4. rsyslogデーモンリブート

`# service rsyslog restart`

<br />

## 5. PLURA V5収集ログ確認

- 全ログ > システム > 主なオブジェクトでapplication確認
<!-- [![image](/docs/images/Ins_G/rsyslog/2.png){: width="800" }](/docs/images/Ins_G/rsyslog/2.png){:target="_blank"} -->

<br />

## 6. PLURA V5リアルタイムで検出フィルタ登録

- 2020010100037 キーワードに対するリアルタイムで検出フィルタ
- フィルタ > 登録フィルタ > システム/ウェブ/ファイアウォール > 登録   
- フィルタ登録下段 > 情報入力 >  msg >  2020010100037 登録
<!-- [![image](/docs/images/Ins_G/rsyslog/3.png){: width="800" }](/docs/images/Ins_G/rsyslog/3.png){:target="_blank"} -->

<br />

**[最新rsyslogインストール]**

`# cp /etc/yum.repos.d/rsyslog.repo /etc/yum.repos.d/rsyslog.repo.old`

`# curl -s http://rpms.adiscon.com/v8-stable/rsyslog.repo -o /etc/yum.repos.d/rsyslog.repo`

`# yum -y install rsyslog`

`# yum list rsyslog`

`# rsyslogd -version`

rsyslogd 8.2012.0 (aka 2020.12) compiled ...

<br />

**[外部参考サイト]**

[https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html](https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html){:target="_blank"}
