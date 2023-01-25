---
title: Redisログ
permalink: ja_redis_cent_log.html
sidebar: Install_A_S_ja
topnav: topnav_ja
---


## 1. redis.conf修正

     > 事前Syslogインストール必要
     > Config位置確認

     loglevel notice
     syslog-enabled yes
     syslog-facility local7

<br />

## 2. Redisデーモンリブート

`# service redis restart`

<br />

## 3. PLURA V5で確認

ログ例 : 全ログ > システム

[![image](/docs/images/Ins_G/redis_c/1.png){: width="800" }](/docs/images/Ins_G/redis_c/1.png){:target="_blank"}

上記の内容を活用し、フィルタを登録すると検出ログを確認出来ます。 
[(Syslogフィルタ登録ショートカット)](https://qubitsec.github.io/ja_f_regi_syslog.html){:target="_blank"}