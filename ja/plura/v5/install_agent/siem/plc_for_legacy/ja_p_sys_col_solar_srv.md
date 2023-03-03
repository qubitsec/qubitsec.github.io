---
title: Solaris Server
permalink: ja_p_sys_col_solar_srv.html
sidebar: Install_A_S_ja
topnav: topnav_ja
---

必ずwww.plura.io右上のInstall Agentsページで確認してインストールしてください。

<br />

## 1. PLURA V5 Agentインストール

Syslogを受け取るLinux系のシステムにPLURA V5 Agentをインストールします。

ページ右上メニューでOS別選択

 - PLURA Log Collector (PLC) > Systemウェブ
 
<br />

## 2. Solaris SrvからSyslog転送設定

`# vi /etc/syslog.conf`

     <例>
     *.info @ログ取り込みシステムIPアドレス

<br />

`# svcadm restart system-log`

     @ 一つはUDP通信
     @@ 二つはTCP通信
     PLURA V5デフォルトは@UDP通信

<br />

## 3. システム登録

- **システム > システム管理 > 取り込みシステム選択 > システム登録**
<!-- [![image](/docs/images/Ins_G/Solaris/Solaris_Srv.png)](/docs/images/Ins_G/Solaris/Solaris_Srv.png){:target="_blank"} -->