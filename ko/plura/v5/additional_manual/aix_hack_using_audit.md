---
title: (AIX) Audit을 이용한 해킹 탐지
permalink: aix_hack_using_audit.html
sidebar: Add_M
topnav: topnav
---

#### 1. 파일 감사 설정하기 [(바로가기)](http://blog.plura.io/?p=10831){: target="_blank"}

#### 2. 파밍 공격 탐지

     PLURA V5 서비스는 파밍 공격을 탐지할 수 있습니다.

2-1. /etc/hosts 파일의 접근하여 위변조를 시도하는 경우,

[![image](/docs/images/Additianal/aix/1.png)](/docs/images/Additianal/aix/1.png){: target="_blank"}


2-2.  PLURA V5 서비스에서 탐지할 수 있습니다.

[![image](/docs/images/Additianal/aix/2.png)](/docs/images/Additianal/aix/2.png){: target="_blank"}

 

#### 3. 홈페이지 위변조 공격 탐지

     PLURA V5 서비스는 홈페이지 위변조 공격을 탐지할 수 있습니다.

3-1. /www/html/index.html 파일의 접근하여 위변조를 시도하는 경우,

[![image](/docs/images/Additianal/aix/3.png)](/docs/images/Additianal/aix/3.png){: target="_blank"}

3-2. PLURA V5 서비스에서 탐지할 수 있습니다.

[![image](/docs/images/Additianal/aix/4.png)](/docs/images/Additianal/aix/4.png){: target="_blank"}