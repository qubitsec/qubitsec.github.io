---
title: Application
permalink: ko_logcol_application.html
sidebar: Install_A_S
product: Install_A_S
---

     PLURA Log Collector (PLC) - Application의 역할

     1. 다른 시스템의 Application log 를 취합
     2. 취합한 Application log 를 압축하고 암호화하여 PLURA V5 클라우드로 전송

<br />

PLURA Log Collector (PLC) 지원 OS는 다음과 같습니다.

[https://qubitsec.github.io/ko_support_os.html](https://qubitsec.github.io/ko_support_os.html){:target="_blank"}

<br />

     제조사가 지원을 종료한 제품에 대하여 PLURA V5에서도 지원을 종료합니다.
     PLURA V5에서 지원하지 않는 운영체제 버전을 사용한다면 문제가 발생할 수 있습니다.
     제조사가 지원 종료한 버전을 사용 중이라면 업그레이드에 대하여 보다 적극적인 검토가 필요합니다. 해킹과 장애 등 다양한 문제에 직면하고 심각한 문제로 발전할 수 있기 때문입니다.

<br />

## PLURA Log Collector (PLC) – Application 설정하기

<br />

### 1. 원격지(자식) 서버에 응용프로그램 전송 모듈 설치


[![image](/docs/images/Ins_G/LogCol_app/app_1.png){: width="800" }](/docs/images/Ins_G/LogCol_app/app_1.png){: target="_blank"}

<br />

### 2. 로그 취합서버(부모)에 PLC 설치(by root)

`# sudo -s`

`# curl https://repo.plura.io/v5/PLC/install.sh | bash`

<br />

### 3. 로그 취합서버(부모)에서 인바운드 TCP 5514 포트를 오픈

<br />

### 4. 로그 취합서버(부모)에서 라이센스 등록 및 실행

[![image](/docs/images/Ins_G/LogCol_app/app_3.png){: width="800" }](/docs/images/Ins_G/LogCol_app/app_3.png){: target="_blank"}

<br />

### 5. 원격지(자식) 서버 등록

- 시스템  > 시스템 관리 > 로그 취합서버(부모) 선택 > 응용프로그램 버튼을 클릭합니다.
[![image](/docs/images/Ins_G/LogCol_app/app_4.png){: width="800" }](/docs/images/Ins_G/LogCol_app/app_4.png){: target="_blank"}

- 시스템 등록 팝업 > 원격지(자식) 서버 정보를 입력합니다.
[![image](/docs/images/Ins_G/LogCol_app/app_5.png)](/docs/images/Ins_G/LogCol_app/app_5.png){: target="_blank"}

<br />

- 등록 팝업에서 “경로 등록” 버튼을 클릭합니다.
[![image](/docs/images/Ins_G/LogCol_app/app_6.png)](/docs/images/Ins_G/LogCol_app/app_6.png){: target="_blank"}

<br />

- 태그 및 경로를 등록합니다.
[![image](/docs/images/Ins_G/LogCol_app/app_7.png)](/docs/images/Ins_G/LogCol_app/app_7.png){: target="_blank"}   

- 태그 등록 방법
   - 응용 프로그램 로그 수집 설정을 위한 태그를 등록할 수 있습니다.
   - 경로 : 관리 > 목록 > 응용프로그램 태그 
   [![image](/docs/images/Ins_G/LogCol_app/app_8.png){: width="800" }](/docs/images/Ins_G/LogCol_app/app_8.png){: target="_blank"}

<br />

- 등록한 태그 및 수집하고자 하는 응용 프로그램 경로를 등록합니다.   
   - 아래 예시에서는 Apache-errorlog를 설정하였습니다.
   [![image](/docs/images/Ins_G/LogCol_app/app_9.png)](/docs/images/Ins_G/LogCol_app/app_9.png){: target="_blank"}

<br />

- 로그 취합서버(부모)를 선택하여 응용프로그램 로그수집이 정상적으로 설정되었는지 확인합니다.   
   - 원격지(자식) 서버를 선택하면 설정 팝업이 노출됩니다.
   [![image](/docs/images/Ins_G/LogCol_app/app_10.png){: width="800" }](/docs/images/Ins_G/LogCol_app/app_10.png){: target="_blank"}

<br />

- 응용프로그램 설정 버튼을 OFF → ON으로 활성화시켜줍니다. 
[![image](/docs/images/Ins_G/LogCol_app/app_11.png)](/docs/images/Ins_G/LogCol_app/app_11.png){: target="_blank"}

<br />

### 6. 수집된 로그 확인

- 전체로그 > 응용프로그램 메뉴에서 수집된 로그를 확인할 수 있습니다.
[![image](/docs/images/Ins_G/LogCol_app/app_12.png){: width="800" }](/docs/images/Ins_G/LogCol_app/app_12.png){: target="_blank"}