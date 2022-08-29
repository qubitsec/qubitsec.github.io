---
title: Redis 로그
permalink: ko_redis_ubuntu_log.html
sidebar: Install_A_S
product: Install_A_S
---


## 1. redis.conf 수정

     > 사전 Syslog 설치 필요
     > Config 위치 확인

     loglevel notice
     syslog-enabled yes
     syslog-facility local7

<br />

## 2. Redis 데몬 재시작

`# service redis restart`

<br />

## 3. PLURA V5에서 확인

로그 예시 : 전체로그 > 시스템

[![image](/docs/images/Ins_G/redis_u/1.png){: width="800" }](/docs/images/Ins_G/redis_u/1.png){:target="_blank"}

위 내용을 활용해서 필터를 등록하면 탐지로그를 확인할 수 있습니다.   
[(Syslog 필터등록 바로가기)](https://qubitsec.github.io/ko_f_regi_syslog.html){:target="_blank"}