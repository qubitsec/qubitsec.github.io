---
title: MySQL(CentOS) 로그
permalink: mysql_log.html
sidebar: Install_A_S
product: Install_A_S
---

## MySQL(CentOS) 로그 분석

### 1. mysql.conf 다운로드 rsyslog 사용

     curl https://repo.plura.io/v5/module/rsyslog/80-mysql.conf -o /etc/rsyslog.d/80-mysql.conf

### 2. 80-mysql.conf 수정

     > mysql error 로그 위치 확인

     #vi /etc/rsyslog.d/80-mysql.conf

### 3. rsyslog 데몬 재 시작

     service rsyslog restart

### 4. PLURA V5에서 확인하기

[![image](/docs/images/Ins_G/Mysql(cent)log/1.png){: width="800" }](/docs/images/Ins_G/Mysql(cent)log/1.png){:target="_blank"}

위 내용을 활용해서 필터를 등록하면 탐지로그를 확인할 수 있습니다.[Syslog 필터등록 바로가기](http://blog.plura.io/?p=7059){:target="_blank"}