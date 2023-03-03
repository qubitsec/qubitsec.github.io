---
title: AIX Server
permalink: ja_p_sys_col_aix_srv.html
sidebar: Install_A_S_ja
topnav: topnav_ja
---

必ずwww.plura.io右上のInstall Agentsページで確認してインストールしてください。

<br />

## 1. PLURA V5 Agentインストール

Syslogを受け取るLinux系のシステムにPLURA V5 Agentをインストールします。

ページ右上メニューでOS別選択

 - PLURA Log Collector (PLC) > Systemタップ

<br />

## 2. AIX SrvからSyslog転送設定

`# vi /etc/syslog.conf`

     <例>
     *.info @ログ取り込みシステムIPアドレス

<br />

`# refresh -s syslogd`

     @ 一つはUDP通信
     @@ 二つはTCP通信
     PLURA V5デフォルトは@UDP通信

<br />

## 3. ファイルの監査設定

ファイルの監査設定は下記の通り設定します。

`# vi /etc/security/audit/config`
     
     set binmode = off
     streammode = on

     class:
     system = USER_Remove,USER_Create,GROUP_Create,GROUP_Remove
     init = User_Login

     users:
     root = general
     default = general, system, init

`# find /etc -type f | awk ‘{printf(“%s:\n\tw = FILE_Write\n\n”,$1)}’ >> /etc/security/audit/objects`

`# /usr/sbin/auditstream | /usr/sbin/auditselect -e “event == FILE_Write” | auditpr -hhelpPRtTc -v > /dev/console &`

`# vi /etc/security/audit/streamcmds/usr/sbin/auditstream | auditpr -v | /usr/bin/logger -p local7.info &`

`# audit off`

`# audit shutdown`

`# refresh -s syslogd`

<br />

## 4. システム登録

- **システム > システム管理 > 取り込みシステム選択 > システム登録**
<!-- [![image](/docs/images/Ins_G/P_Sys_Collector_AIX_Srv/システム登録.png)](/docs/images/Ins_G/P_Sys_Collector_AIX_Srv/システム登録.png){:target="_blank"} -->