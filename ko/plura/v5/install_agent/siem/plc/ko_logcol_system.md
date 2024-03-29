---
title: System
permalink: ko_logcol_system.html
sidebar: Install_A_S
product: Install_A_S
---


     PLURA Log Collector (PLC) - System의 역할

     1. 다른 시스템의 syslog 를 취합
     2. 취합한 syslog 를 압축하고 암호화하여 PLURA V5 클라우드로 전송

<br />

PLURA Log Collector (PLC) 지원 OS는 다음과 같습니다.

[https://qubitsec.github.io/ko_support_os.html](https://qubitsec.github.io/ko_support_os.html){:target="_blank"}

<br />

     제조사가 지원을 종료한 제품에 대하여 PLURA V5에서도 지원을 종료합니다.
     PLURA V5에서 지원하지 않는 운영체제 버전을 사용한다면 문제가 발생할 수 있습니다.
     제조사가 지원 종료한 버전을 사용 중이라면 업그레이드에 대하여 보다 적극적인 검토가 필요합니다. 해킹과 장애 등 다양한 문제에 직면하고 심각한 문제로 발전할 수 있기 때문입니다.

<br />

## PLURA Log Collector (PLC) – System 설정하기

<br />

### 1. 원격지(자식) 서버에 Syslog 전송 설정

<br />

__※ 자식 호스트 설정하기__

Syslog 전송 설정 (by root)

`# vi /etc/rsyslog.conf`

     <예>

     *.info @로그취합호스트IP

<br />

Syslog 재시작

`# service rsyslog restart`

<br />

### 2. 로그 취합서버(부모)에 PLC 설치(by root)


`# sudo -s`

`# curl https://repo.plura.io/v5/PLC/install.sh | bash`

<br />

### 3. 라이센스 등록 및 실행

`# /etc/plura/plura.sh register 라이센스키`

<br />

### 4. 원격지(자식) 서버 등록

- 시스템  > 시스템 관리 > 로그 취합서버(부모) 선택 > 호스트 버튼을 클릭합니다.
[![image](/docs/images/Ins_G/logCol_system/sys_3.png){: width="800" }](/docs/images/Ins_G/logCol_system/sys_3.png){:target="_blank"}

<br />

- 등록 팝업 > 원격지(자식) 서버 정보를 입력합니다.
[![image](/docs/images/Ins_G/logCol_system/sys_4.png)](/docs/images/Ins_G/logCol_system/sys_4.png){:target="_blank"}

<br />

- 시스템 > 시스템 관리 페이지에서 원격지(자식) 서버가 등록되었습니다. 
[![image](/docs/images/Ins_G/logCol_system/sys_5.png){: width="800" }](/docs/images/Ins_G/logCol_system/sys_5.png){:target="_blank"}

<br />

### 5. 수집된 로그 확인

- 전체로그 > 호스트 메뉴에서 수집된 로그를 확인할 수 있습니다.
<!--
[![image](/docs/images/Ins_G/logCol_system/sys_6.png){: width="800" }](/docs/images/Ins_G/logCol_system/sys_6.png){:target="_blank"}
-->
