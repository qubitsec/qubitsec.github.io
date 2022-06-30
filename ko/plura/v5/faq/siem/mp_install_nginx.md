---
title: Nginx 수동 설치
permalink: mp_install_nginx.html
sidebar: faq_siem_M
topnav: topnav
---

## 1. 사전 조사

### 1-1) nginx 실행 여부 검사

`# ps -ef|grep nginx`

     nginx 실행파일 경로/ 명령 파라미터 확인 (=readlink /proc/$(pid)/exe)

     nginx 설정파일 경로 확인 (nginx -t)
     
     nginx process owner 확인

<br />

### 1-2) 서비스 등록 확인

`# service nginx status`

<br />

### 1-3) 재설정 실험

`# service nginx reload`

`# nginx -s`

<br />

### 1-4) 설정 파일 확인

     /etc/nginx/nginx.conf
     http {
     include conf.d/*.conf
     …

     → include conf.d/*.conf 라인 없으면 추가 !!!
     (nginx 설정파일 경로)/conf.d 디렉토리 없으면 생성 !!!

<br />

## 2. 표준 설치

`# curl https://repo.plura.io/v4/module/nginx/plura.conf -o /etc/nginx/conf.d/plura.conf`

     → http {} 블럭에 access_log 지시어 라인이 추가되어 웹로그가 생성됩니다.

<br />

## 3. 사용자 정의 설치

⭐주의 !!! server {} 블럭에 access_log 지시어가 있는 경우, 상위 블록인 http {} 블럭의 access_log
지시어가 무시됩니다. 따라서 아래와 같이, 수동으로 access_log 지시어 라인을 추가해야 합니다.

     server {
     access_log /var/log/plura/weblog.log mod_plura;

<br />

## 4. 정보 등록

`# echo ModPlura-Nginx > /etc/modplura`

`# echo 5.5.0 >> /etc/modplura`

`# echo /usr/sbin/nginx >> /etc/modplura`

`# echo /etc/nginx >> /etc/modplura`

`# touch /etc/.modplura`

<br />

## 5. 권한 이슈
⭐주의 !!! PLURA 웹로그 생성 디렉토리의 owner를 nginx worker process 의 owner로 변경합니다.

`# chown nginx /var/log/plura`