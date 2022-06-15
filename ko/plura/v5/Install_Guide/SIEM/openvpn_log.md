---
title: Openvpn 로그 분석
permalink: openvpn_log.html
sidebar: Install_G_S
product: Install_G_S
---

### 1. openvpn.conf 다운로드 rsyslog 사용

     curl https://repo.plura.io/v5/module/rsyslog/80-openvpn.conf -o /etc/rsyslog.d/80-openvpn.conf

### 2. 80-openvpn.conf 수정

     > /etc/openvpn/server/server.conf 로그 위치 확인

     log /var/log/openvpn.log
     log-append /var/log/openvpn.log

     #vi /etc/rsyslog.d/80-openvpn.conf

### 3. openvpn server conf 수정

     > logging 레벨 확인

     verb 4

     #vi /etc/openvpn/server/server.conf

### 4. rsyslog 데몬 재 시작

     service rsyslog restart

### 5. PLURA V5에서 확인하기

![image](/docs/images/Ins_G/openvpn/1.png){: width="680" height="250"}

위 내용을 활용해서 필터를 등록하면 탐지로그를 확인할 수 있습니다.[(Syslog 필터등록 바로가기)](http://blog.plura.io/?p=7059){:target="_blank"}