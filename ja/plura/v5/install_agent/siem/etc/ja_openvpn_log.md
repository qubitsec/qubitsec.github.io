---
title: Openvpnログ
permalink: ja_openvpn_log.html
sidebar: Install_A_S
product: Install_A_S
---

## 1. openvpn.confダウンロードrsyslog使用

`# curl https://repo.plura.io/v5/module/rsyslog/80-openvpn.conf -o /etc/rsyslog.d/80-openvpn.conf`

<br />

## 2. 80-openvpn.conf修正

`# /etc/openvpn/server/server.conf`ログ位置確認

log /var/log/openvpn.log

log-append /var/log/openvpn.log

`# vi /etc/rsyslog.d/80-openvpn.conf`

<br />

## 3. openvpn server conf修正

loggingレベル確認

verb 4

`# vi /etc/openvpn/server/server.conf`

<br />

## 4. rsyslogデーモンリブート

`# service rsyslog restart`

<br />

## 5. PLURA V5で確認

ログ例 : 全ログ > システム

[![image](/docs/images/Ins_G/openvpn/1.png){: width="800" }](/docs/images/Ins_G/openvpn/1.png){:target="_blank"}

上記の内容を活用し、フィルターを登録すると検出ログが確認出来ます。
[(Syslogフィルター登録ショートカット)](https://qubitsec.github.io/ko_f_regi_syslog.html){:target="_blank"}