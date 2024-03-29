---
title: xrdp 로그
permalink: ko_xrdp_log.html
sidebar: Install_A_S
product: Install_A_S
---

## 1. xrdp.conf 다운로드 rsyslog 사용

`# curl https://repo.plura.io/v5/module/rsyslog/80-xrdp.conf -o /etc/rsyslog.d/80-xrdp.conf`

<br />

## 2. 80-xrdp.conf 수정

     > /etc/xrdp/xrpd.ini 로그 위치 확인

     [Logging] LogFile=xrdp.log
     LogLevel=DEBUG
     EnableSyslog=true
     SyslogLevel=DEBUG
     > /etc/xrdp/sesman.ini 로그 위치 확인

     [Logging] LogFile=xrdp-sesman.log
     LogLevel=DEBUG
     EnableSyslog=1
     SyslogLevel=DEBUG

     # vi /etc/rsyslog.d/80-xrdp.conf

<br />

## 3. rsyslog 데몬 재 시작

`# service rsyslog restart`

<br />

## 4. PLURA V5에서 확인하기

로그 예시 : 전체로그 > 호스트

[![image](/docs/images/Ins_G/xrdp/1.png){: width="800" }](/docs/images/Ins_G/xrdp/1.png){:target="_blank"}

<br />

[![image](/docs/images/Ins_G/xrdp/2.png){: width="800" }](/docs/images/Ins_G/xrdp/2.png){:target="_blank"}

위 내용을 활용해서 필터를 등록하면 탐지로그를 확인할 수 있습니다.   
[(필터등록 바로가기)](https://qubitsec.github.io/ko_f_regi_syslog.html){:target="_blank"}
