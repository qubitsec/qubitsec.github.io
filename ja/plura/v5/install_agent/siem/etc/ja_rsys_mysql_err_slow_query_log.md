---
title: (PLC)MySQL Error & Slow-Queryログ
permalink: ja_rsys_mysql_err_slow_query_log.html
sidebar: Install_A_S_ja
topnav: topnav_ja
---

      Rsyslog : MySQL ErrorログとSlow-Queryの取り込するみための設定

<br />

## 1. rsyslog conf設定

### 1-1. 設定

`# vi /etc/rsyslog.d/80-mysql.conf`

     #variables required for non-syslog log file forwarding – mysql error
     #edit on your location

     input(type=”imfile”
     File=”/var/log/mysqld.log”
     Tag=”mysqld-errors”
     Severity=”error”
     Facility=”local7″)

     input(type=”imfile”
     File=”/var/log/mysql-slow.log”
     Tag=”mysql-slow”
     Severity=”notice”
     Facility=”local7″)

     ###### Creates a template for each log file in the Logentries UI
     ### logic to apply the relevant templates to the different log files

     if $programname == ‘mysqld-errors’ then /var/log/plura/ceelog-127.0.0.1.log;CEETemplate
     :programname, isequal, “mysqld-errors” ~

     if $programname == ‘mysql-slow’ then /var/log/plura/ceelog-127.0.0.1.log;CEETemplate
     :programname, isequal, “mysql-slow” ~

<br />

rsyslog restart

`# systemctl restart rsyslog`

<br />

### 1-2. PLURA V5 repoからダウンロード

`# wget https://repo.plura.io/v5/module/rsyslog/80-mysql.conf`

`# curl https://repo.plura.io/v5/module/rsyslog/80-mysql.conf -o /etc/rsyslog.d/80-mysql.conf`

<br />

## 2. MySQL – SLOW QUERY設定

<br />

### 2-1. 設定

`# vi /etc/my.cnf`

[mysqld]

slow_query_log = 1

slow_query_log_file = /var/log/mysql-slow.log

long_query_time = 3

<br />

### 2-2. ログファイル生成及び権限設定

`# touch /var/log/mysql-slow.log`

`# chown mysql.mysql /var/log/mysql-slow.log`

<br />

### 2-3. 権限確認

`# ls -aZ /var/log/mysql*`

<!-- [![image](/docs/images/Ins_G/rsys_mysql/1.png)](/docs/images/Ins_G/rsys_mysql/1.png){:target="_blank"} -->

<br />

### 2-4. mysql restart

`# systemctl restart mysqld`

<br />

### 2-5. アクティブ確認

`mysql> show variables like ‘slow_query_%’;`

<!-- [![image](/docs/images/Ins_G/rsys_mysql/2.png)](/docs/images/Ins_G/rsys_mysql/2.png){:target="_blank"} -->

<br />

## 3. ログ確認

Error又はSlow Query発生後、システムログからMySQLに対するログを確認

ログ例 : 全ログ > システム

<!-- [![image](/docs/images/Ins_G/rsys_mysql/3.png){: width="800" }](/docs/images/Ins_G/rsys_mysql/3.png){:target="_blank"} -->

<br />

外部参考サイト

[https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html](https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html){:target="_blank"}