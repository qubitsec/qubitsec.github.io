---
title: Apache httpd error 로그
permalink: ko_apache_httpd_log.html
sidebar: Install_A_S
product: Install_A_S
---

      Apache httpd error 로그 수집

<br />

### 1. conf 설정하기(rsyslog 사용)
80-httpd.conf → conf 파일 생성하기

`# cd /etc/rsyslog.d/`   
`# vi /etc/rsyslog.d/80-httpd.conf`

<br />

### 2. conf 파일 생성
File = “로그 경로”, Tag = “태그”, Severity = “심각도”, programname = “프로그램명”

`# vi /etc/rsyslog.d/80-httpd.conf`

     #variables required for non-syslog log file forwarding – httpd error log file
     #edit on your location

     input(type=”imfile”
     File=”/var/log/httpd/error_log”
     Tag=”httpd”
     Severity=”error”
     Facility=”local7″)

     ###### Creates a template for each log file in the Logentries UI
     ### logic to apply the relevant templates to the different log files

     if $programname == ‘httpd‘ then /var/log/plura/ceelog-127.0.0.1.log;CEETemplate
     :programname, isequal, ‘httpd‘ stop

<br />

#### 2-1. PLURA V5 repo 에서 다운로드 받기

`# wget https://repo.plura.io/v5/module/rsyslog/80-httpd.conf`

`# curl https://repo.plura.io/v5/module/rsyslog/80-httpd.conf -o /etc/rsyslog.d/80-httpd.conf`

<br />

### 3. rsyslog 데몬 재시작

`# service rsyslog restart`

<br />

### 4. PLURA V5 탐지 확인
[![image](/docs/images/Ins_G/apache_httpd_err/1.png){: width="800px"}](/docs/images/Ins_G/apache_httpd_err/1.png){: target="_blank"}


위 내용을 활용해서 필터를 등록하면 탐지로그를 확인할 수 있습니다.
[Syslog 필터등록](https://qubitsec.github.io/ko_f_regi_syslog.html){:target="_blank"}

<br />

외부 참고 사이트

[https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html](https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html){:target="_blank"}