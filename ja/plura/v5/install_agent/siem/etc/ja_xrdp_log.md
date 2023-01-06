---
title: xrdpログ
permalink: ja_xrdp_log.html
sidebar: Install_A_S
product: Install_A_S
---

## 1. xrdp.confダウンロードrsyslog使用

`# curl https://repo.plura.io/v5/module/rsyslog/80-xrdp.conf -o /etc/rsyslog.d/80-xrdp.conf`

<br />

## 2. 80-xrdp.conf修正

     > /etc/xrdp/xrpd.iniログ位置確認

     [Logging] LogFile=xrdp.log
     LogLevel=DEBUG
     EnableSyslog=true
     SyslogLevel=DEBUG
     > /etc/xrdp/sesman.iniログ位置確認

     [Logging] LogFile=xrdp-sesman.log
     LogLevel=DEBUG
     EnableSyslog=1
     SyslogLevel=DEBUG

     # vi /etc/rsyslog.d/80-xrdp.conf

<br />

## 3. rsyslogデーモンリブート

`# service rsyslog restart`

<br />

## 4. PLURA V5から確認

ログ例 : 全ログ > システム

[![image](/docs/images/Ins_G/xrdp/1.png){: width="800" }](/docs/images/Ins_G/xrdp/1.png){:target="_blank"}

<br />

[![image](/docs/images/Ins_G/xrdp/2.png){: width="800" }](/docs/images/Ins_G/xrdp/2.png){:target="_blank"}

上記の内容を活用し、フィルターを登録すると検出ログが確認出来ます。
[(Syslogフィルター登録ショートカット)](https://qubitsec.github.io/ko_f_regi_syslog.html){:target="_blank"}
