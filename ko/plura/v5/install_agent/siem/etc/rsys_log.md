---
title: (PLC)응용프로그램 로그
permalink: rsys_log.html
sidebar: Install_A_S
product: Install_A_S
---

응용프로그램 로그 中 특별한 키워드를 실시간 탐지하고 싶은 경우 어떻게 하면 될까요?

예를 들어, 아래와 같은 응용프로그램 로그 中 __2020010100037__ 키워드를 실시간 탐지할 경우입니다.

## 1. 수집되는 로그 확인하기

[![image](/docs/images/Ins_G/rsyslog/1.png)](/docs/images/Ins_G/rsyslog/1.png){:target="_blank"}

## 2. conf 설정하기(rsyslog 사용)
※ 80-application.conf → conf 파일 생성하기

     # vi /etc/rsyslog.d/80-application.conf

## 3. conf 파일 생성 예시

※ File = “로그 경로”, Tag = “로그 태그”, Severity = “심각도”
※ 파일명에 와일드카드를 사용해야 하는 경우는 __rsyslog 버전 8.25 이상__ 을 사용하셔야 합니다.
※ 최신 rsyslog 설치하기 바로가기

     #variables required for non-syslog log file forwarding – application log file
     #edit on your location

     input(type=”imfile”
     File=”/var/log/application.log”
     Tag=”application”
     Severity=”info”
     Facility=”local7″)

     ###### Creates a template for each log file in the Logentries UI
     ### logic to apply the relevant templates to the different log files

     if $programname == “application” then /var/log/plura/ceelog-127.0.0.1.log;CEETemplate
     :programname, isequal, “application” ~

## 3-1. PLURA V5 repo 에서 다운로드 받기

     # wget https://repo.plura.io/v5/module/rsyslog/80-application.conf

     # curl https://repo.plura.io/v5/module/rsyslog/80-application.conf -o /etc/rsyslog.d/80-application.conf

## 4. rsyslog 데몬 재시작

    # service rsyslog restart 

## 5. PLURA V5 수집 로그 확인

     전체로그 > 시스템 > 주요개체 컬럼에서 application 확인

<br />
[![image](/docs/images/Ins_G/rsyslog/2.png){: width="800" }](/docs/images/Ins_G/rsyslog/2.png){:target="_blank"}

## 6. PLURA V5 실시간 탐지 필터 등록하기

     1) 2020010100037 키워드에 대한 실시간 탐지 등록 필터

     2) 필터 > 등록필터 > 시스템/웹/웹방화벽 > 등록

     3) 필터등록 하단 > 정보입력 >  msg >  2020010100037 등록


<br />
[![image](/docs/images/Ins_G/rsyslog/3.png){: width="800" }](/docs/images/Ins_G/rsyslog/3.png){:target="_blank"}



**[최신 rsyslog 설치하기]**

      # cp /etc/yum.repos.d/rsyslog.repo /etc/yum.repos.d/rsyslog.repo.old

      # curl -s http://rpms.adiscon.com/v8-stable/rsyslog.repo -o /etc/yum.repos.d/rsyslog.repo

      # yum -y install rsyslog

      # yum list rsyslog

      # rsyslogd -version

      rsyslogd 8.2012.0 (aka 2020.12) compiled with:
      
- 외부 참고 사이트

[https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html](https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html){:target="_blank"}
