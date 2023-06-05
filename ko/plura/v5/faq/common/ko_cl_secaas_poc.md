---
title: 온라인 PoC 진행 방법 안내
permalink: ko_cl_secaas_poc.html
sidebar: faq_common_M
topnav: topnav
---

## 1. PLURA PoC 진행 프로세스 안내

<br />

> 계정 생성   
> 로그인 後 고객지원 요청 신청   
> 동료 초대   
> 에이전트 설치 (Install Agents)

<br />

### 1-1. PLURA 계정 생성

- 무료 평가판 시작(크롬 브라우저 권장)
   - [https://www.plura.io/signup/](https://www.plura.io/signup/){: target="_blank"}

<!--
[![image](/docs/images/Additianal/cloud/1.png){: width="800" }](/docs/images/Additianal/cloud/1.png){: target="_blank"}
-->

- 이메일 승인 > 가입 완료 (체험 라이선스 14일)
- 체험 라이선스 연장 필요

<br />

### 1-2. 고객지원 요청

- 로그 분석 지원을 위해 계정생성 완료 後 다음과 같이 “고객지원 요청하기” 선택
   - 요청 사유 작성, 예) PoC 로그 분석 요청
   - 메뉴위치: 좌측 상단 > 관리 > 서비스 > 고객지원 요청하기   
   [https://qubitsec.github.io/ko_manage_service.html](https://qubitsec.github.io/ko_manage_service.html){: target="_blank"}

[![image](/docs/images/Additianal/cloud/2.png){: width="800" }](/docs/images/Additianal/cloud/2.png){: target="_blank"}

<br />

### 1-3. 동료 초대
- PoC에 함께 참여하는 동료 초대
- 분석하는 시스템에 대한 통합 관리 제공
- 메뉴 위치: 좌측 상단 > 관리 > 멤버 > 멤버 추가
[https://qubitsec.github.io/ko_manage_member.html](https://qubitsec.github.io/ko_manage_member.html){: target="_blank"}

<br />

## 2. 에이전트 설치

### 2-1. 로그인 後 에이전트 설치 “Install Agents”

- Install Agents 페이지 안내 또는 에이전트 설치 영상을 참고하여 에이전트 설치   

<!--
- 윈도우 서버에 에이전트 설치 예시   
[https://qubitsec.github.io/ko_p_agent_win_srv.html](https://qubitsec.github.io/ko_p_agent_win_srv.html){: target="_blank"}
-->

- 윈도우 에이전트 설치 예시   
[https://qubitsec.github.io/ko_p_agent_edr_win.html](https://qubitsec.github.io/ko_p_agent_edr_win.html){: target="_blank"}

<br />

### 2-2. 사전 환경 확인
- Install Agents 에서 시스템 환경에 맞는 문서를 찾기 어렵다면 대상 서버들의 OS 버전, 웹서버 App, 웹서비스 포트 정보 확인   
- 해당 내역에 따라 정확한 설치 페이지를 안내해 드립니다.

<br />

### 2-3. 에이전트 설치 – 원격지원

- 필요한 사전 정보   

  - 대상 서버의 접속정보 (root 권한 필요)   
  - 대상 서버의 OS 버전, 웹서버 App, 웹서비스 포트 정보 (예 : CentOS 7 / Apache 2.4 / TCP 80)
  - Windows 의 경우 Sysmon 을 설치하시면 보다 상세한 로그를 확인할 수 있으니 설치를 권장   
Sysmon 설치 가이드 : [https://qubitsec.github.io/ko_sysmon.html](https://qubitsec.github.io/ko_sysmon.html){: target="_blank"}

<br />
 
## 3. PLURA 매뉴얼
- [https://qubitsec.github.io/](https://qubitsec.github.io/){: target="_blank"}
