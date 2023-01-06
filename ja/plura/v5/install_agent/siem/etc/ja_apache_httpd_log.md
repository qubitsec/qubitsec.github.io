---
title: Apache httpd error ログ
permalink: ja_apache_httpd_log.html
sidebar: Install_A_S
product: Install_A_S
---

      Apache httpd errorログ収集

<br />

### 1. conf設定(rsyslog使用)
80-httpd.conf → confファイル生成

`# cd /etc/rsyslog.d/`   
`# vi /etc/rsyslog.d/80-httpd.conf`

<br />

### 2. confファイル生成
File = “ログパス”, Tag = “タグ”, Severity = “深刻度”, programname = “プログラム名”

`# vi /etc/rsyslog.d/80-httpd.conf`

     #variables required for non-syslog log file forwarding – httpd error log file
     #edit on your location

     input(type=”imfile”
     File=”/var/log/httpd/error_log”
     Tag=”httpd”
     Severity=”error”
     Facility=”local7″)

     ###### Creates a template for each log file in the Logentries UI
     ### logic to apply the relevant templates to the different log files

     if $programname == ‘httpd‘ then /var/log/plura/ceelog-127.0.0.1.log;CEETemplate
     :programname, isequal, ‘httpd‘ stop

<br />

#### 2-1. PLURA V5 repoからダウンロード

`# wget https://repo.plura.io/v5/module/rsyslog/80-httpd.conf`

`# curl https://repo.plura.io/v5/module/rsyslog/80-httpd.conf -o /etc/rsyslog.d/80-httpd.conf`

<br />

### 3. rsyslogデーモンリブート

`# service rsyslog restart`

<br />

### 4. PLURA V5検出確認

ログ例 : 全ログ > システム

[![image](/docs/images/Ins_G/apache_httpd_err/1.png){: width="800px"}](/docs/images/Ins_G/apache_httpd_err/1.png){: target="_blank"}


上の内容を活用してフィルターを登録すると検出ログが確認出来ます。

[Syslogフィルターを登録](https://qubitsec.github.io/ko_f_regi_syslog.html){:target="_blank"}

<br />

外部参考サイト

[https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html](https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html){:target="_blank"}