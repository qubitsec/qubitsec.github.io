---
title: Audit 설정 안내
permalink: ko_chk_file_audit_log_set.html
sidebar: faq_siem_M
topnav: topnav
---

## 1. AIX 에서 Remote Logging 설정하기

PLURA V5 우측 상단의 Install Agents 페이지 상단 메뉴에서 OS별 선택

 UNIX > AIX탭
 
 <br />

## 2. 파일 감사 설정하기

**Audit > config 설정값 변경**

 audit service 종료

`# audit off`

`# audit shutdown`

<br />

 config 수정

`# vi /etc/security/audit/config`

      // 값 변경

      set binmode = off

      streammode = on

      // 입력값 추가(class section, user section)

      class:

      system = USER_Remove,USER_Create,GROUP_Create,GROUP_Remove

      init = User_Login

      …

      users:

      root = general

      default = general, system, init

<br />

`# /etc/security/audit/streamcmds`

      // 입력값 추가

      /usr/sbin/auditstream | auditpr -v | /usr/bin/logger -p local7.info &

      find /etc -type f | awk ‘{printf(“%s:\n\tw = FILE_Write\n\n”,$1)}’ >> /etc/security/audit/objects

      /usr/sbin/auditstream | /usr/sbin/auditselect -e “event == FILE_Write” | auditpr  -hhelpPRtTc -v > /dev/console &

<br />

`# vi /etc/security/audit/objects`

      /etc/hosts:

      w = FILE_Write

<br />

**> Audit Tag Name 설정**

`# vi /etc/security/audit/objects`

      /etc/hosts:

      w = W_@태그네임

<br />

`# vi /etc/security/audit/events`

      W_@태그네임 = printf “%s_qubit”

<br />

## 3. Syslog module 구성

 config 수정

`# vi /etc/syslog.conf `

      // 입력값 추가

      *.info @로그취합서버 IP주소

      *.debug @로그취합서버 IP주소

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

## 4. PLURA V5 웹에서 Audit 필터 등록

PLURA V5 웹에서 Audit 필터를 등록합니다. [(바로가기)](https://qubitsec.github.io/ko_f_regi_audit.html){: target="_blank"}

<br />

## 5. PLURA V5 에서 Audit 필터 탐지 활용 

[(바로가기)](https://qubitsec.github.io/ko_aix_hack_using_audit.html){: target="_blank"}

<br />

참조   
[https://developer.ibm.com/technologies/systems/articles/au-audit_filter/](https://developer.ibm.com/technologies/systems/articles/au-audit_filter/){: target="_blank"}