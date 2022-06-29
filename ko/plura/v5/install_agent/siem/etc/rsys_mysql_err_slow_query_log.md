---
title: (PLC)MySQL Error & Slow-Query 로그
permalink: rsys_mysql_err_slow_query_log.html
sidebar: Install_A_S
product: Install_A_S
---

MySQL Error 로그와 Slow-Query 취합을 위한 설정

<br />

## 1. rsyslog conf 설정

     1) 설정
     vi /etc/rsyslog.d/80-mysql.conf

     #variables required for non-syslog log file forwarding – mysql error
     #edit on your location

     input(type=”imfile”
     File=”/var/log/mysqld.log”
     Tag=”mysqld-errors”
     Severity=”error”
     Facility=”local7″)

     input(type=”imfile”
     File=”/var/log/mysql-slow.log”
     Tag=”mysql-slow”
     Severity=”notice”
     Facility=”local7″)

     ###### Creates a template for each log file in the Logentries UI
     ### logic to apply the relevant templates to the different log files

     if $programname == ‘mysqld-errors’ then /var/log/plura/ceelog-127.0.0.1.log;CEETemplate
     :programname, isequal, “mysqld-errors” ~

     if $programname == ‘mysql-slow’ then /var/log/plura/ceelog-127.0.0.1.log;CEETemplate
     :programname, isequal, “mysql-slow” ~

     2) rsyslog restart
     # systemctl restart rsyslog

<br />

### 1-1. PLURA V5 repo 에서 다운로드 받기

     # wget https://repo.plura.io/v5/module/rsyslog/80-mysql.conf

     # curl https://repo.plura.io/v5/module/rsyslog/80-mysql.conf -o /etc/rsyslog.d/80-mysql.conf

<br />

## 2. MySQL – SLOW QUERY 설정

     1) 설정
     vi /etc/my.cnf

     [mysqld]
     slow_query_log = 1
     slow_query_log_file = /var/log/mysql-slow.log
     long_query_time = 3

     2) 로그 파일 생성 및 권한 설정
     # touch /var/log/mysql-slow.log
     # chown mysql.mysql /var/log/mysql-slow.log

     3) 권한 확인
     # ls -aZ /var/log/mysql*

<br />
[![image](/docs/images/Ins_G/rsys_mysql/1.png)](/docs/images/Ins_G/rsys_mysql/1.png){:target="_blank"}
<br />

      4) mysql restart
      # systemctl restart mysqld

     5) 활성화 확인
     mysql> show variables like ‘slow_query_%’;
<br />
[![image](/docs/images/Ins_G/rsys_mysql/2.png)](/docs/images/Ins_G/rsys_mysql/2.png){:target="_blank"}

<br />

## 3. 로그 확인

     Error 또는 Slow Query 발생 후 시스템 로그에서 MySQL 관련 로그를 확인

<br />
[![image](/docs/images/Ins_G/rsys_mysql/3.png){: width="800" }](/docs/images/Ins_G/rsys_mysql/3.png){:target="_blank"}
<br />
외부 참고 사이트

[https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html](https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html){:target="_blank"}