---
title: AIX Server
permalink: ko_p_sys_col_aix_srv.html
sidebar: Install_A_S
product: Install_A_S
---

반드시 www.plura.io 우측 상단의 Install Agents 페이지에서 확인하여 설치하시길 바랍니다.

<br />

## 1. PLURA V5 Agent 설치

Syslog 를 전달받을 Linux 계열의 시스템에 PLURA V5 Agent를 설치합니다.

페이지 상단 메뉴에서 OS별 선택

 - Log Collector > System 탭

<br />

## 2. AIX Srv 에서 Syslog 전송 설정

`# vi /etc/syslog.conf`

     <예>
     *.info @로그취합 시스템 IP주소

<br />

`# refresh -s syslogd`

     @ 하나는 UDP로 통신
     @@ 두개는 TCP로 통신
     PLURA V5는 기본 @UDP 통신

<br />

## 3. 파일 감사 설정

파일 감사 설정을 하려면 아래와 같이 설정합니다.

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

## 4. 시스템 등록

- **시스템 > 시스템 관리 > 취합시스템 선택 > 시스템 등록**

[![image](/docs/images/Ins_G/P_Sys_Collector_AIX_Srv/시스템등록.png)](/docs/images/Ins_G/P_Sys_Collector_AIX_Srv/시스템등록.png){:target="_blank"}