---
title: Apache 서버에서 HTTP 압축 비활성화
permalink: apache_http_compression.html
sidebar: faq_siem_M
topnav: topnav
---

     웹서버에서 HTTP 압축을 비활성화 하여 운영하면 PLURA V5 에서 데이터 유출 행위를 탐지할 수 있습니다.
     다음은 Apache 서버에서 HTTP가 압축되고 있는지 확인하고 압축을 비활성화하는 방법입니다.

<br />

## 1. HTTP 압축을 위한 서버 테스트

 헤더에 다음 요청을 추가하여 HTTP 압축을 확인합니다.

     Accept-Encoding:compress,gzip

 압축이 활성화 되어있으면 서버는 압축된 페이지를 응답하고, 압축을 지원하지 않고 있는 경우에는 일반 텍스트로 응답합니다.

 <br />

## 2. CentOS/Red Hat 에서 HTTP 압축 비활성화

`# sudo vi /etc/httpd/conf/httpd.conf`

     #LoadModule deflate_module modules/mod_deflate.so
     (해당 라인을 주석 처리)

`# service httpd restart`

<br />

## 3. Ubuntu 에서 HTTP 압축 비활성화

`# sudo a2dismod deflate`

`# sudo /etc/init.d/apache2 restart`

<br />

▣ 참고자료

 PLURA V5 의 데이터유출 탐지 예외 사항과 해결책

[데이터유출 탐지 예외 사항과 해결책](https://qubitsec.github.io/data_exfiltration_solution.html){: target="_blank"}