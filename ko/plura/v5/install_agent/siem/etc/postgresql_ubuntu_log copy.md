---
title: PostgreSQL(Ununtu) 로그
permalink: postgresql_ubuntu_log.html
sidebar: Install_A_S
product: Install_A_S
---

## 1. postgresql.conf 수정

     > 사전 Syslog 설치 필요
     > Config 위치 확인

     [config 경로 예시] /var/lib/pgsql/9.6/data/postgresql.conf
     [수정 예시] # ERROR REPORTING AND LOGGING 하단에서 수정
     log_destination = ‘stderr’ 라인을 주석처리
     log_destination = ‘syslog’ 라인 추가

     # These are relevant when logging to syslog: 하단의 다음 4라인 주석 해제
     #syslog_facility = ‘LOCAL0’
     #syslog_ident = ‘postgres’
     #syslog_sequence_numbers = on
     #syslog_split_messages = on

<br />

## 2. PostgreSQL 및 Syslog 재시작

`# systemctl restart postgresql`

`# systemctl restart rsyslog`

<br />

## 3. PLURA V5에서 확인

[![image](/docs/images/Ins_G/Postgresql_u/1.png){: width="800" }](/docs/images/Ins_G/Postgresql_u/1.png){:target="_blank"}

위 내용을 활용해서 필터를 등록하면 탐지로그를 확인할 수 있습니다.[(Syslog 필터등록 바로가기)](https://qubitsec.github.io/f_regi_syslog.html){:target="_blank"}