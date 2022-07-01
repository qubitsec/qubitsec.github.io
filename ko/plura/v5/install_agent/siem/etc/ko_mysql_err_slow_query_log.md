---
title: MySQL Error & Slow-Query 로그
permalink: ko_mysql_err_slow_query_log.html
sidebar: Install_A_S
product: Install_A_S
---


[응용프로그램] MySQL Error 로그와 Slow-Query 로그 취합을 위한 설정

<br />

## 1. 응용프로그램 로그 수집 설정

### 1-1. 시스템  > 시스템 관리 > 서버 선택 > 설정 탭 이동 > 설정 버튼을 클릭합니다.

[![image](/docs/images/Ins_G/mysql_slow/1.png){: width="800" }](/docs/images/Ins_G/mysql_slow/1.png){:target="_blank"}

<br />

### 1-2. 응용프로그램 원본로그 수집 설정을 활성화합니다.

[![image](/docs/images/Ins_G/mysql_slow/2.png){: width="800" }](/docs/images/Ins_G/mysql_slow/2.png){:target="_blank"}

<br />

### 1-3. 경로 > 설정 버튼을 클릭합니다.

[![image](/docs/images/Ins_G/mysql_slow/3.png){: width="800" }](/docs/images/Ins_G/mysql_slow/3.png){:target="_blank"}

<br />

### 1-4. 태그 선택 및 경로를 입력합니다.
MySQL Error 로그와 Slow-Query 로그 경로를 입력합니다.

[![image](/docs/images/Ins_G/mysql_slow/4.png)](/docs/images/Ins_G/mysql_slow/4.png){:target="_blank"}

<br />

### 1-5. 태그가 정상적으로 등록되었는지 확인 후, 수정 버튼을 클릭합니다.

[![image](/docs/images/Ins_G/mysql_slow/5.png)](/docs/images/Ins_G/mysql_slow/5.png){:target="_blank"}

※ 태그 등록 방법

- 경로 : 관리 > 목록 > 응용프로그램 태그 : 응용 프로그램 로그 수집 설정을 위한 태그를 등록할 수 있습니다.

[![image](/docs/images/Ins_G/mysql_slow/6.png){: width="800" }](/docs/images/Ins_G/mysql_slow/6.png){:target="_blank"}

<br />

- 등록 버튼을 클릭합니다.

[![image](/docs/images/Ins_G/mysql_slow/7.png){: width="800" }](/docs/images/Ins_G/mysql_slow/7.png){:target="_blank"}

<br />

- 등록하고자 하는 태그를 입력합니다.

[![image](/docs/images/Ins_G/mysql_slow/8.png){: width="800" }](/docs/images/Ins_G/mysql_slow/8.png){:target="_blank"}

<br />

## 2. MySQL – SLOW QUERY 설정

### 2.1. 설정

`# vi /etc/my.cnf`

[mysqld]

slow_query_log = 1

slow_query_log_file = /var/log/mysql-slow.log

long_query_time = 3

<br />

### 2.2. 로그 파일 생성 및 권한 설정

`# touch /var/log/mysql-slow.log`

`# chown mysql.mysql /var/log/mysql-slow.log`

<br />

### 2.3. 권한 확인

`# ls -aZ /var/log/mysql*`

[![image](/docs/images/Ins_G/mysql_slow/9.png)](/docs/images/Ins_G/mysql_slow/9.png){:target="_blank"}

### 2.4. mysql restart

`# systemctl restart mysqld`

<br />

### 2.5. 활성화 확인
`mysql> show variables like ‘slow_query_%’;`

[![image](/docs/images/Ins_G/mysql_slow/10.png)](/docs/images/Ins_G/mysql_slow/10.png){:target="_blank"}

<br />

## 3. 로그 확인

Mysql Error 또는 Slow Query 로그 발생 후 응용프로그램 로그에서 MySQL 관련 로그를 확인합니다.   
등록한 태그명으로 검색이 가능합니다.

내부 블로그 

[응용프로그램 로그 업로드 설정하기](https://qubitsec.github.io/set_app_log_up.html){:target="_blank"}