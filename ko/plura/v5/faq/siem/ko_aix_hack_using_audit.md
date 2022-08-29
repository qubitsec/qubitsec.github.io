---
title: Audit을 이용한 해킹 탐지
permalink: ko_aix_hack_using_audit.html
sidebar: faq_siem_M
topnav: topnav
---

## 1. 파일 감사 설정하기 

[(바로가기)](https://qubitsec.github.io/ko_chk_file_audit_log_set.html){: target="_blank"}

<br />

## 2. 파밍 공격 탐지
PLURA V5 서비스는 파밍 공격을 탐지할 수 있습니다.

<br />

### 2-1. /etc/hosts 파일의 접근하여 위변조를 시도하는 경우

[![image](/docs/images/Additianal/aix/1.png){: width="800" }](/docs/images/Additianal/aix/1.png){: target="_blank"}

<br />

### 2-2.  PLURA V5에서 탐지

[![image](/docs/images/Additianal/aix/2.png){: width="800" }](/docs/images/Additianal/aix/2.png){: target="_blank"}

<br />

## 3. 홈페이지 위변조 공격 탐지
PLURA V5 서비스는 홈페이지 위변조 공격을 탐지할 수 있습니다.

<br />

### 3-1. /www/html/index.html 파일의 접근하여 위변조를 시도하는 경우

[![image](/docs/images/Additianal/aix/3.png){: width="800" }](/docs/images/Additianal/aix/3.png){: target="_blank"}

<br />

### 3-2. PLURA V5에서 탐지

[![image](/docs/images/Additianal/aix/4.png){: width="800" }](/docs/images/Additianal/aix/4.png){: target="_blank"}