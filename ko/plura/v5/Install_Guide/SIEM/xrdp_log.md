---
title: xrdp 로그 분석
permalink: xrdp_log.html
sidebar: Install_G_S
product: Install_G_S
---

#### 1. xrdp.conf 다운로드 rsyslog 사용

     curl https://repo.plura.io/v5/module/rsyslog/80-xrdp.conf -o /etc/rsyslog.d/80-xrdp.conf

#### 2. 80-xrdp.conf 수정

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
     #vi /etc/rsyslog.d/80-xrdp.conf

#### 3. rsyslog 데몬 재 시작

     service rsyslog restart

#### 4. PLURA V5에서 확인하기

![image](/docs/images/Ins_G/xrdp/1.png){: width="700" height="300"}
![image](/docs/images/Ins_G/xrdp/2.png){: width="700" height="300"}

위 내용을 활용해서 필터를 등록하면 탐지로그를 확인할 수 있습니다.[(Syslog 필터등록 바로가기)](http://blog.plura.io/?p=7059){:target="_blank"}
