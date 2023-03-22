---
title: Audit設定案内
permalink: ja_chk_file_audit_log_set.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

## 1. AIXでRemote Logging設定

PLURA V5右上のInstall Agentsページ上段メニューからOS別選択

 UNIX > AIXタブ
 
 <br />

## 2. ファイル監査設定

**Audit > config設定値変更**

 audit service終了

`# audit off`

`# audit shutdown`

<br />

 config修正

`# vi /etc/security/audit/config`

      // 値変更

      set binmode = off

      streammode = on

      // 入力値追加(class section, user section)

      class:

      system = USER_Remove,USER_Create,GROUP_Create,GROUP_Remove

      init = User_Login

      …

      users:

      root = general

      default = general, system, init

<br />

`# /etc/security/audit/streamcmds`

      // 入力値追加

      /usr/sbin/auditstream | auditpr -v | /usr/bin/logger -p local7.info &

      find /etc -type f | awk ‘{printf(“%s:\n\tw = FILE_Write\n\n”,$1)}’ >> /etc/security/audit/objects

      /usr/sbin/auditstream | /usr/sbin/auditselect -e “event == FILE_Write” | auditpr  -hhelpPRtTc -v > /dev/console &

<br />

`# vi /etc/security/audit/objects`

      /etc/hosts:

      w = FILE_Write

<br />

**> Audit Tag Name設定**

`# vi /etc/security/audit/objects`

      /etc/hosts:

      w = W_@タグ名

<br />

`# vi /etc/security/audit/events`

      W_@タグ名 = printf “%s_qubit”

<br />

## 3. Syslog module構成

 config修正

`# vi /etc/syslog.conf `

      // 入力値追加

      *.info @ログ取り込みサーバーIPアドレス

      *.debug @ログ取り込みサーバーIPアドレス

      …

      *.debug;*.emerg;*.alert;*.crit;*.err;*.warning;*.notice;*.info;mail.none;auth.none  /var/adm/syslog/syslog.log

      #User.debug /var/adm/syslog/syslog.log rotate size 5m files 5

<br />

 restart src

`# refresh -s syslogd`

<br />

 start audit

`# audit off`

`# audit start`

<br />

## 4. PLURA V5ウェブでAuditフィルタ登録

PLURA V5ウェブでAuditフィルタを登録します。 [(ショートカット)](https://qubitsec.github.io/ja_f_regi_audit.html){: target="_blank"}

<br />

## 5. PLURA V5でAuditフィルタ検出活用 

[(ショートカット)](https://qubitsec.github.io/ja_aix_hack_using_audit.html){: target="_blank"}

<br />

参照   
[https://developer.ibm.com/technologies/systems/articles/au-audit_filter/](https://developer.ibm.com/technologies/systems/articles/au-audit_filter/){: target="_blank"}