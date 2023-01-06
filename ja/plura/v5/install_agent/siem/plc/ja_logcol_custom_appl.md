---
title: Custom
permalink: ja_logcol_custom_appl.html
sidebar: Install_A_S
product: Install_A_S
---

## アプリケーション分析 – Postfix映像

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/YmWLsadlIdM' frameborder='0' allowfullscreen></iframe></div>

<br />

PLURA V5はアプリケーションに対するログをアップロード設定を使用して収集出来ます。

     1. アプリケーション原本ログのアップロードのためには管理 > リスト > アプリケーションタグを登録する必要があります。
     2. 収集するパスを把握する必要があります。

<br />

アプリケーションログアップロード設定[1]

[https://qubitsec.github.io/ko_set_app_log_up.html](https://qubitsec.github.io/ko_set_app_log_up.html){:target="_blank"}

<br />

**アプリケーションログは“LogStash”を使用してカラムを分離出来ます。**

- Logstashには多様なソースからデータを収集、転換して目標の腕先へ転送出来るようにする軽量のオープンソースサーバー側のデータ処理パイプラインです。

- Logstashを使用するとシステムログ, ウェブサイトログ, アプリケーションサーバーログなど多様なデータ原本から非定型データを簡単に収集出来ます。[2]

<br />

## 1. Logstash設定方法

<br />

### 1-1. Install Logstash
[https://github.com/QubitSecurity/Logstash](https://github.com/QubitSecurity/Logstash){:target="_blank"}

<br />

### 1-2. Confファイルダウンロード
`# cd /etc/logstash/conf.d/`

`# wget “https://raw.githubusercontent.com/QubitSecurity/Logstash/main/conf.d/70-postfix-plura.conf”`

<br />

### 1-3. Postfixログパス修正

`# vi /etc/logstash/conf.d/70-postfix-plura.conf`

[https://github.com/QubitSecurity/Logstash/blob/main/conf.d/70-postfix-plura.conf](https://github.com/QubitSecurity/Logstash/blob/main/conf.d/70-postfix-plura.conf){:target="_blank"}

[![image](/docs/images/Ins_G/LogCol_Customapp/2.png){: width="800" }](/docs/images/Ins_G/LogCol_Customapp/2.png){:target="_blank"}

`# mkdir /etc/logstash/patterns.d`

`# cd /etc/logstash/patterns.d`

`# wget “https://raw.githubusercontent.com/QubitSecurity/Logstash/main/patterns.d/grok-postfix”`

<br />

## 2. PLURA-Agentを使用してアップロード設定

上記から説明したLogstashを使用してLinux : PostfixログをPLURA V5で収集します。

- テスト環境
   - 遠距離サーバー(子) : CentOS Linux release 7.9.2009 (Core), Postfix, Logstashインストール
   - ログ取り込みサーバー(親) : CentOS Linux release 7.9.2009 (Core),ライセンス登録及び実行

<br />

[Install Guide > SIEM > PLURA Log Collector (PLC) > Application[3] : [https://qubitsec.github.io/ko_logcol_application.html](https://qubitsec.github.io/ko_logcol_application.html){:target="_blank"}

<br />

### 2-1. Logstashが設定された遠距離(子)サーバー登録

<br />

### 2-2. アプリケーションサーバー登録

- システム  > システム管理 > ログ取り込みサーバー(親)選択 > アプリケーションボタンをクリックします。 
[![image](/docs/images/Ins_G/LogCol_Customapp/3.png){: width="800" }](/docs/images/Ins_G/LogCol_Customapp/3.png){:target="_blank"}

<br />

### 2-3. システム登録ポップアップ > 遠隔地(子)サーバー情報入力

- アプリケーションのカスタマイズログ収集パスに“/var/log/plura/app-logstash-postfix.log”を入力します。
[![image](/docs/images/Ins_G/LogCol_Customapp/4.png)](/docs/images/Ins_G/LogCol_Customapp/4.png){:target="_blank"}

<br />

### 2-4. Logstash実行

- システム管理でパス設定まで完了した後、Logstashを実行します。

RUN Logstash(foreground)

[![image](/docs/images/Ins_G/LogCol_Customapp/5.png){: width="800" }](/docs/images/Ins_G/LogCol_Customapp/5.png){:target="_blank"}

<br />

## 3. PLURA V5ウェブで確認

- パス : 全ログ > アプリケーション > カスタマイズ > postfix

- 管理 > 使用 > アプリケーション > カスタマイズ設定がON状態の場合、メニューが出ます。[4]
[![image](/docs/images/Ins_G/LogCol_Customapp/6.png){: width="800" }](/docs/images/Ins_G/LogCol_Customapp/6.png){:target="_blank"}

<br />

- “修正”ボタンをクリックした後, postfix項目にチェックすればカスタマイズアプリケーションでpostfixログが確認出来ます。
[![image](/docs/images/Ins_G/LogCol_Customapp/7.png){: width="800" }](/docs/images/Ins_G/LogCol_Customapp/7.png){:target="_blank"}

<br />

- Postfixログが生成されるとPLURA V5全ログ(アプリケーション)で確認出来ます。
[![image](/docs/images/Ins_G/LogCol_Customapp/8.png){: width="800" }](/docs/images/Ins_G/LogCol_Customapp/8.png){:target="_blank"}

<br />

## 4. 参考サイト

[1] アプリケーションログアップロード設定 : [https://qubitsec.github.io/ko_set_app_log_up.html](https://qubitsec.github.io/ko_set_app_log_up.html){:target="_blank"}

[2] Logstash定義 : [https://aws.amazon.com/ko/opensearch-service/the-elk-stack/logstash/](https://aws.amazon.com/ko/opensearch-service/the-elk-stack/logstash/){:target="_blank"}

[3] Install Guide > SIEM > PLC > Application : [https://qubitsec.github.io/ko_logcol_application.html](https://qubitsec.github.io/ko_logcol_application.html){:target="_blank"}

[4] Manual > Common > 管理 > 使用 : [https://qubitsec.github.io/ko_manage_use.html](https://qubitsec.github.io/ko_manage_use.html){:target="_blank"}