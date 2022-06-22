---
title: Redis(CentOS) 로그
permalink: redis_cent_log.html
sidebar: Install_A_S
product: Install_A_S
---


## 1. redis.conf 수정

     > 사전 Syslog 설치 필요
     > Config 위치 확인

     loglevel notice
     syslog-enabled yes
     syslog-facility local7

## 2. Redis 데몬 재시작

     service redis restart

## 3. PLURA V5에서 확인

     로그 샘플 예)

<br />
[![image](/docs/images/Ins_G/redis_c/1.png){: width="800" }](/docs/images/Ins_G/redis_c/1.png){:target="_blank"}

위 내용을 활용해서 필터를 등록하면 탐지로그를 확인할 수 있습니다.[(Syslog 필터등록 바로가기)](https://qubitsec.github.io/f_regi_syslog.html){:target="_blank"}