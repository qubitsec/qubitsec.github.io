---
title: MySQLログ
permalink: ja_mysql_log.html
sidebar: Install_A_S
product: Install_A_S
---

     MySQL(CentOS)ログ分析

<br />

### 1. mysql.confダウンロードrsyslog使用

`# curl https://repo.plura.io/v5/module/rsyslog/80-mysql.conf -o /etc/rsyslog.d/80-mysql.conf`

<br />

### 2. 80-mysql.conf修正

mysql errorログ位置確認

`# vi /etc/rsyslog.d/80-mysql.conf`

<br />

### 3. rsyslogデーモンリブート

`# service rsyslog restart`

<br />

### 4. PLURA V5で確認

ログ例 : 全ログ > システム

[![image](/docs/images/Ins_G/Mysql(cent)log/1.png){: width="800" }](/docs/images/Ins_G/Mysql(cent)log/1.png){:target="_blank"}

上記の内容を活用し、フィルターを登録すると検出ログが確認出来ます。
[Syslogフィルター登録ショートカット](https://qubitsec.github.io/ko_f_regi_syslog.html){:target="_blank"}