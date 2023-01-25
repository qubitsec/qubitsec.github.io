---
title: PostgreSQLログ
permalink: ja_postgresql_cent_log.html
sidebar: Install_A_S_ja
topnav: topnav_ja
---


## 1. postgresql.conf修正

    > 事前Syslogインストール必要
    > Config位置確認

     [configパス例] /var/lib/pgsql/9.6/data/postgresql.conf
     [修正例] # ERROR REPORTING AND LOGGING下段で修正
     log_destination = ‘stderr’ラインを注釈処理
     log_destination = ‘syslog’ライン追加

     # These are relevant when logging to syslog:下段の次の4行注釈解除
     #syslog_facility = ‘LOCAL0’
     #syslog_ident = ‘postgres’
     #syslog_sequence_numbers = on
     #syslog_split_messages = on

<br />

## 2. PostgreSQL及びSyslogリブート

バージョンによってサービス名が違うのでバージョン確認

`# psql –version`

     [バージョン出力例] psql (PostgreSQL) 9.6.15
     [サービス名確認パス例] /etc/systemd/system/multi-user.target.wants/postgresql-9.6.service
     [上記の例で確認されたバージョンのよるリブート例] service postgresql-9.6 restart
     
`# service rsyslog restart`

<br />

## 3. PLURA V5で確認

ログ例 : 全ログ > システム

[![image](/docs/images/Ins_G/Postgresql_c/1.png){: width="800" }](/docs/images/Ins_G/Postgresql_c/1.png){:target="_blank"}
<br />

上記の内容を活用し、フィルタを登録すると検出ログが確認出来ます。 
[(Syslogフィルタ登録ショートカット)](https://qubitsec.github.io/ja_f_regi_syslog.html){:target="_blank"}