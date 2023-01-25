---
title: FreeBSD Server
permalink: ja_p_sys_col_freebsd_srv.html
sidebar: Install_A_S_ja
topnav: topnav_ja
---

必ずwww.plura.io右上のInstall Agentsページで確認してインストールしてください。

<br />

## 1. PLURA V5 Agent インストール

Syslogを受け取るLinux系のシステムにPLURA V5 Agentをインストールします。

ページ右上メニューでOS別選択

  - PLURA Log Collector (PLC) > Systemタップ

<br /> 

## 2. FreeBSD SrvからSyslog転送設定

`# vi /etc/syslog.conf`

     <예>
     *.info @ログ取り込みシステムIPアドレス

<br />

`# /etc/rc.d/syslogd restart`

     @ 一つはUDP通信
     @@ 二つはTCP通信
     PLURA V5はデフォルト@UDP通信

<br />

## 3. システム登録

- **システム > システム管理 > 取り込みシステム選択 > システム登録**
 [![image](/docs/images/Ins_G/FreeBSD/freebsd.png)](/docs/images/Ins_G/FreeBSD/freebsd.png){:target="_blank"}