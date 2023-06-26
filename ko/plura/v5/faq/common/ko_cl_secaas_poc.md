---
title: 온라인 PoC 진행 방법 안내
permalink: ko_cl_secaas_poc.html
sidebar: faq_common_M
topnav: topnav
---


     PLURA V5 사용을 위한 진행 안내입니다.
     회원 가입 > 로그인 > EDR 에이전트 설치로 진행되며 3分 내로 완료됩니다.

<br>


## 1. PLURA PoC 진행 개요

<br>

(1) 회원 가입에 따른 계정 생성 <br>
(2) 로그인 後 고객지원 요청 신청 <br>
(3) 에이전트 설치 (Install Agents)

<br>

### 1-1. PLURA 계정 생성

- 무료 평가판 시작 <br>
   - [https://www.plura.io/signup/](https://www.plura.io/signup/){: target="_blank"}

<!--
[![image](/docs/images/Additianal/cloud/1.png){: width="800" }](/docs/images/Additianal/cloud/1.png){: target="_blank"}
-->

- 이메일 승인 > 가입 완료 (무료 평가판 라이선스 14일)
- 요청 시 평가판 라이선스 연장 제공

<br>

### 1-2. 고객지원 요청

- 로그 분석 지원을 위해 계정생성 완료 後 다음과 같이 “고객지원 요청하기” 선택
   - 요청 사유 작성, 예) 해킹 공격 탐지 및 대응
   - 메뉴위치: 좌측 상단 메뉴 PLURA V5 옆 > 관리 > 서비스 > 고객지원 요청하기
   [https://qubitsec.github.io/ko_manage_service.html](https://qubitsec.github.io/ko_manage_service.html){: target="_blank"}

[![image](/docs/images/Additianal/cloud/2.png){: width="800" }](/docs/images/Additianal/cloud/2.png){: target="_blank"}

<br>

### 1-3. 동료 초대
- 로그인 계정에 동료 초대
- 분석 대상 시스템에 대한 통합 관리 제공
- 메뉴 위치: 좌측 상단 > 관리 > 멤버 > 멤버 추가
[https://qubitsec.github.io/ko_manage_member.html](https://qubitsec.github.io/ko_manage_member.html){: target="_blank"}

<br>

## 2. 에이전트 설치

### 2-1. 로그인 後 에이전트 설치 “Install Agents”

- Install Agents 페이지 안내 또는 에이전트 설치 영상을 참고하여 에이전트 설치

<!--
- 윈도우 서버에 에이전트 설치 예시   
[https://qubitsec.github.io/ko_p_agent_win_srv.html](https://qubitsec.github.io/ko_p_agent_win_srv.html){: target="_blank"}
-->

- 윈도우 에이전트 설치 예시   
[https://qubitsec.github.io/ko_p_agent_edr_win.html](https://qubitsec.github.io/ko_p_agent_edr_win.html){: target="_blank"}

<br>

### 2-2. 사전 환경 확인
- "Install Agents" 에서 시스템 환경에 맞는 문서를 찾기 어렵다면 대상 서버들의 OS 버전, 웹서버 종류 및 버전, 웹서비스 포트 정보 확인   
- 해당 내역에 따라 정확한 설치 페이지를 안내해 드립니다.

<br>

### 2-3. 에이전트 설치 – 원격지원

- 필요한 사전 정보   

  - 대상 서버의 접속정보 (윈도우 사용자 권한, 리눅스 root 권한)   
  - 대상 서버의 OS 버전, 웹서버 종류 및 버전, 웹서비스 포트 정보 (예 : CentOS 8 / Apache 2.4 / TCP 80)
  - Windows 의 경우 Sysmon 설치해야 보다 정확하고 충분한 이상징후 탐지가 가능합니다.
Sysmon 설치 가이드 : [https://qubitsec.github.io/ko_sysmon.html](https://qubitsec.github.io/ko_sysmon.html){: target="_blank"}

<br>
 
## 3. PLURA V5 매뉴얼
- [https://qubitsec.github.io/](https://qubitsec.github.io/){: target="_blank"}
