---
title: 데모 공격 시나리오 
permalink: ko_demo_attack_scenario.html
sidebar: faq_siem_M
topnav: topnav
---

     PLURA V5를 이용하시는 고객 또는 파트너사가 간단한 명령어 수행으로 탐지 로그를 발생시킬 수 있습니다.

### 마이터 어택 & 상관분석 & 시스템

**PLURA V5 에이전트가 설치된 리눅스 환경에서 아래의 명령어를 입력하면 마이터 어택과 시스템 탐지 로그를 확인할 수 있습니다.**

``# useradd Demo``

[![image](/docs/images/Additianal/demoattack/01.png)](/docs/images/Additianal/demoattack/01.png){: target="_blank"}

<br />

PLURA V5 필터탐지 > 시스템 메뉴에서 탐지

[![image](/docs/images/Additianal/demoattack/02.png){: width="800" }](/docs/images/Additianal/demoattack/02.png){: target="_blank"}

<br />

``# userdel Demo``

[![image](/docs/images/Additianal/demoattack/03.png)](/docs/images/Additianal/demoattack/03.png){: target="_blank"}

<br />

PLURA V5 필터탐지 > 시스템 메뉴에서 탐지

[![image](/docs/images/Additianal/demoattack/04.png){: width="800" }](/docs/images/Additianal/demoattack/04.png){: target="_blank"}

<br />

PLURA V5 보안탐지 > 마이터어택 > 리스트 메뉴에서 탐지

[![image](/docs/images/Additianal/demoattack/05.png){: width="800" }](/docs/images/Additianal/demoattack/05.png){: target="_blank"}

<br />

**상관분석 탐지의 경우, 사전에 상관분석 필터가 등록되어 있어야 합니다.**

※ 상관분석 탐지 샘플

(경로 : 필터 > 보안 > 상관분석 > 필터등록)

- 상관분석 정보(분류, 필터명, 설명 등)를 입력

- 상관분석 Group 추가 버튼 클릭

- 시스템/웹 필터 추가 버튼 클릭

아래 필터의 경우, 시스템 단일 필터 추가 “운영체제 : centos, 필터명 : 계정 생성(M5919j9igmyqbg9h)&계정 삭제”

[![image](/docs/images/Additianal/demoattack/06.png){: width="800" }](/docs/images/Additianal/demoattack/06.png){: target="_blank"}

<br />

아래 명령어를 순차적으로 입력하여 계정 생성 및 삭제 필터로 조합한 상관분석 필터를 탐지하겠습니다.

``# useradd Demo``

[![image](/docs/images/Additianal/demoattack/07.png)](/docs/images/Additianal/demoattack/07.png){: target="_blank"}

<br />

``# userdel Demo``

[![image](/docs/images/Additianal/demoattack/08.png)](/docs/images/Additianal/demoattack/08.png){: target="_blank"}

<br />

PLURA V5 보안탐지 > 상관분석 메뉴에서 탐지

[![image](/docs/images/Additianal/demoattack/09.png){: width="800" }](/docs/images/Additianal/demoattack/09.png){: target="_blank"}

<br /> 

### 웹

**웹 필터 탐지를 확인하기 위해서는 데모 공격을 진행할 웹 서버 환경이 필요합니다.**

<br />

PLURA V5 에이전트가 설치된 웹 서버 환경에 Wordpress를 설치한 뒤, 아래의 모의 공격문을 웹 브라우저 창에 입력합니다.

``?<script>alert("xss")</script>``

<br />

[![image](/docs/images/Additianal/demoattack/10.png)](/docs/images/Additianal/demoattack/10.png){: target="_blank"}

<br />

PLURA V5 필터탐지 > 웹 메뉴에서 탐지

[![image](/docs/images/Additianal/demoattack/11.png){: width="800" }](/docs/images/Additianal/demoattack/11.png){: target="_blank"}

<br /> 

### 홈페이지 위변조

**아래의 설명을 참고하여 다양한 운영체제(CentOS, ubuntu, Windows)에서 사용자의 홈페이지 파일명(경로)을 추가 후, 홈페이지 위변조를 탐지할 수 있습니다.**

내부 블로그 : [홈페이지 위변조](https://qubitsec.github.io/ko_s_f_h_forgery.html){: target="_blank"}

1.[에이전트가 설치된 윈도우 환경] C:\ 경로에 임의의 폴더(C:\000) 생성
  
[![image](/docs/images/Additianal/demoattack/12.png)](/docs/images/Additianal/demoattack/12.png){: target="_blank"}

<br />

2.[PLURA 페이지] 필터 > 보안 > 홈페이지위변조 > 윈도우 > 파일 경로(C:\000) 추가
  
[![image](/docs/images/Additianal/demoattack/13.png){: width="800" }](/docs/images/Additianal/demoattack/13.png){: target="_blank"}

<br />

3.[에이전트가 설치된 윈도우 환경] 임의로 생성한 폴더 내에서 txt파일 생성 후, 수정 및 삭제
  
[![image](/docs/images/Additianal/demoattack/14.png)](/docs/images/Additianal/demoattack/14.png){: target="_blank"}

<br />

4.PLURA V5 보안탐지 > 홈페이지 위변조 메뉴에서 탐지
  
[![image](/docs/images/Additianal/demoattack/15.png){: width="800" }](/docs/images/Additianal/demoattack/15.png){: target="_blank"}

<br />

### 데이터 유출 & 계정탈취

- **데이터 유출 : 취약한 웹 서버 환경에서 실제 데이터 유출 공격이 발생하였을 경우, 탐지가 됩니다.**

- **계정탈취 : 수집된 로그를 바탕으로 분석을 한 뒤, 계정탈취 필터를 등록해야 합니다.**
