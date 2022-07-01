---
title: Apache 수동 설치
permalink: ko_mp_install_apache.html
sidebar: faq_siem_M
topnav: topnav
---

## 1. 사전 조사

`# ps -ef|grep httpd`

`# ps -ef|grep apache`

     → apache 실행파일 경로/ 명령 파라미터 확인 (=readlink /proc/$(pid)/exe)
     apache process owner 확인

`httpd|apache2 -V`
     → apache 설정파일 경로 확인

`httpd|apache2 -v`
     → apache 버전 확인

<br />

### 1-1. 서비스 등록 확인

`# service httpd|apache2 status`

<br />

### 1-2. 재설정 실험

`# service httpd|apache2 reload`

`${apache2dir}/bin/apachectl graceful`

`${apache2dir}/bin/httpd -k graceful`

<br />

### 1-3. 설정 파일 확인

표준 설치 = /etc/httpd/conf.d/

     /etc/httpd/conf/httpd.conf
     IncludeOptional conf.d/*.conf

<br />

사용자 정의 설치 = /usr/local/apache2/conf/extra/

     /usr/local/apache2/conf/httpd.conf
     Include conf/extra/plura.conf
     → 마지막 라인에 추가 !!!

<br />

## 2. 표준 설치

`# curl https://repo.plura.io/v4/module/apache/centos/plura.conf -o /etc/httpd/conf.d/plura.conf`

`# curl https://repo.plura.io/v4/module/apache/centos/x86_64/7/2.4/mod_plura_module.so -o /etc/httpd/modules/mod_plura_module.so`

<br />

## 3. 사용자 정의 설치

`# curl https://repo.plura.io/v4/module/apache/centos/plura.conf -o /usr/local/apache2/conf/extra/plura.conf`

`# curl https://repo.plura.io/v4/module/apache/centos/x86_64/7/2.4/mod_plura_module.so -o /usr/local/apache2/modules/mod_plura_module.so`

<br />

plura.conf 파일의 내용

     LoadModule mod_plura_module modules/mod_plura_module.so
     mp_log /var/log/plura/weblog.log

<br />

## 4. 정보 등록

`# echo ModPlura-Apache > /etc/modplura`

`# echo 5.5.3 >> /etc/modplura`

`# echo /usr/sbin/httpd >> /etc/modplura`

`# echo /etc/httpd >> /etc/modplura`

`# echo /etc/httpd >> /etc/modplura`

`# echo centos/x86_64/7/2.4 >> /etc/modplura`

`# touch /etc/.modplura`

<br />

## 5. 사용자 정의 설치

`# echo /usr/local/apache2/bin/httpd >> /etc/modplura`

`# echo /usr/local/apache2 >> /etc/modplura`

`# echo /usr/local/apache2 >> /etc/modplura`

<br />

## 6. 권한 이슈

⭐주의 : PLURA 웹로그 생성 디렉토리의 owner를 apache worker process 의 owner로 변경합니다.

`# chown apache /var/log/plura`

`# chmod 755 /var/log/plura`

`# chmod +x /etc/httpd/modules/mod_plura_module.so`

<br />

⭐selinux 객체 설정

`# chcon -h system_u:object_r:httpd_sys_content_t:s0 /etc/httpd/conf.d/plura.conf`

`# chcon -h system_u:object_r:httpd_sys_content_t:s0 /etc/httpd/modules/mod_plura_module.so`

`# restorecon /etc/httpd/conf.d/plura.conf`

`# restorecon /etc/httpd/modules/mod_plura_module.so`