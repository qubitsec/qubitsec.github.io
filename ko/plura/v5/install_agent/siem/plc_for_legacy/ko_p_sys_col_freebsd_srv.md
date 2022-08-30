---
title: FreeBSD Server
permalink: ko_p_sys_col_freebsd_srv.html
sidebar: Install_A_S
product: Install_A_S
---

반드시 www.plura.io 우측 상단의 Install Agents 페이지에서 확인하여 설치하시길 바랍니다.

<br />

## 1. PLURA V5 Agent 설치

Syslog 를 전달받을 Linux 계열의 시스템에 PLURA V5 Agent를 설치합니다.

페이지 상단 메뉴에서 OS별 선택

  - PLURA Log Collector (PLC) > System 탭

<br /> 

## 2. FreeBSD Srv 에서 Syslog 전송 설정

`# vi /etc/syslog.conf`

     <예>
     *.info @로그취합 시스템 IP주소

<br />

`# /etc/rc.d/syslogd restart`

     @ 하나는 UDP로 통신
     @@ 두개는 TCP로 통신
     PLURA V5는 기본 @UDP 통신

<br />

## 3. 시스템 등록

- **시스템 > 시스템 관리 > 취합 시스템 선택 > 시스템 등록**
 [![image](/docs/images/Ins_G/FreeBSD/freebsd.png)](/docs/images/Ins_G/FreeBSD/freebsd.png){:target="_blank"}