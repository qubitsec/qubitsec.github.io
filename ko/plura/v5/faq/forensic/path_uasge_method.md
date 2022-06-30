---
title: 운영체제 로그 업로드 수집 경로 및 사용 방법
permalink: path_uasge_method.html
sidebar: faq_forensic_M
topnav: topnav
---

     PLURA V5 Forensic은 수집된 시스템(운영체제)의 로그를 업로드하여 분석을 할 수 있는 서비스입니다.

     업로드된 로그는 사전에 정의된 마이터 어택 등 수천개의 이상행위를 탐지할 수 있는 정책에 따라 자동 분석되므로
     종래의 로그 분석 업무 방식 대비 99.9999%이상의 업무 부하를 줄일 수 있습니다.


## 1. 운영체제(OS) 종류별 로그 수집 경로

<br />

### 1-1. 윈도우즈

`C:\Windows\System32\winevt\Logs`

[![image](/docs/images/Additianal/path/1.png){: width="800" }](/docs/images/Additianal/path/1.png){: target="_blank"}

<br />

### 1-2. 리눅스 – Redhat/CentOS 계열

`/var/log/messages`

<br />

### 1-3. 리눅스 – Ubuntu 우분투 계열

`/var/log/syslog`

<br />

## 2. PLURA V5 Forensic 에이전트에서 로그 업로드 하는 방법

<br />

### 2-1. PLURA V5 Forensic Agent 로그인을 합니다.

[![image](/docs/images/Additianal/path/2.png){: width="800" }](/docs/images/Additianal/path/2.png){: target="_blank"}

<br />

### 2-2. 로그 업로드를 진행할 운영체제 및 로그년도를 선택합니다.

[![image](/docs/images/Additianal/path/3.png){: width="800" }](/docs/images/Additianal/path/3.png){: target="_blank"}

<br />

### 2-3. 시스템/호스트명/닉네임을 입력한 후, “Select” 버튼을 클릭하여 로그가 있는 경로를 선택합니다.

[![image](/docs/images/Additianal/path/4.png){: width="800" }](/docs/images/Additianal/path/4.png){: target="_blank"}

<br />

### 2-4. “Start” 버튼을 클릭하여 로그업로드를 진행합니다.

[![image](/docs/images/Additianal/path/5.png){: width="800" }](/docs/images/Additianal/path/5.png){: target="_blank"}

<br />

### 2-5. 로그 업로드가 진행 중에는 “START” 버튼이 “STOP” 버튼으로 변경되며, 업로드를 중지할 수 있습니다.

[![image](/docs/images/Additianal/path/6.png){: width="800" }](/docs/images/Additianal/path/6.png){: target="_blank"}

<br />

### 2-6. 로그업로드가 완료되었습니다.

PLURA V5 에서 정상적으로 업로드 된 로그를 확인해주세요.

[![image](/docs/images/Additianal/path/7.png){: width="800" }](/docs/images/Additianal/path/7.png){: target="_blank"}
 
<br />

      제조사가 지원을 종료한 제품에 대하여 PLURA V5에서도 지원을 종료합니다.  
      PLURA V5에서 지원하지 않는 운영체제 버전을 사용한다면 문제가 발생할 수 있습니다.  
      제조사가 지원 종료한 버전을 사용 중이라면 업그레이드에 대하여 보다 적극적인 검토가 필요합니다.   해킹과 장애 등 다양한 문제에 직면하고 심각한 문제로 발전할 수 있기 때문입니다.

<br />

**내부 블로그**

PLURA V5 Forensic 에이전트 설치 방법

[https://qubitsec.github.io/forensic.html](https://qubitsec.github.io/forensic.html){: target="_blank"}