---
title: HP-UX Server
permalink: ja_p_sys_col_hp_ux_srv.html
sidebar: Install_A_S
product: Install_A_S
---

必ずwww.plura.io右上のInstall Agentsページで確認してインストールしてください。

<br />

## 1. PLURA V5 Agent 설치

Syslogを受け取るLinux系のシステムにPLURA V5 Agentをインストールします。

ページ右上メニューでOS別選択

  - PLURA Log Collector (PLC) > Systemタップ
 
<br />

## 2. HP-UX SrvからSyslog転送設定

`# vi /etc/syslog.conf`

     <例>
     *.info @ログ取り込みシステムIPアドレス

`# /sbin/init.d/syslogd stop`

`# /sbin/init.d/syslogd start`

<br />

     @ 一つはUDP通信
     @@ 二つはTCP通信
     PLURA V5デフォルトは@UDP通信

<br />

## 3. システム登録

- **システム > システム管理 > 取り込みシステム選択 > システム登録**
 [![image](/docs/images/Ins_G/P_Sys_Collector_HP-UX_Srv/HP_UX.png)](/docs/images/Ins_G/P_Sys_Collector_HP-UX_Srv/HP_UX.png){:target="_blank"}