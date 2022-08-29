---
title: Wail2ban 에 의한 윈도우 방화벽 설정 
permalink: ko_win_fw_registration_wail2ban.html
sidebar: faq_siem_M
topnav: topnav
---

     Wail2ban 을 이용해 RDP 무차별 대입공격에 대한 보안 설정을 했을 경우, Wail2ban 에 의해 윈도우 방화벽에 차단 등록되는 동작을 PLURA V5에서 탐지할 수 있습니다.

<br />

Wail2ban 이란?

[https://developer.ibm.com/kr/cloud/softlayer-bluemix-infra/security/2017/08/31/rdp-security-script/](https://developer.ibm.com/kr/cloud/softlayer-bluemix-infra/security/2017/08/31/rdp-security-script/){: target="_blank"}

<br />

## 1. 필터 등록 예시

PLURA V5 웹에서 필터 등록으로 설정 방법

**필터 > 등록 > 시스템 > 등록하기**

**서버그룹 선택 > 운영체제 windows 선택 > Security 채널 선택 > 이벤트타입 선택**

[![image](/docs/images/Additianal/wail/1.png){: width="800" }](/docs/images/Additianal/wail/1.png){: target="_blank"}

이벤트 타입에서 방화벽 예외 목록 변경 규칙 추가(4946) 선택

그림과 같이 선택 후 ‘데이터 값’에 wail2ban block 을 넣고 하단의 ‘등록’ 버튼 클릭

<br />

## 2. 방화벽 등록 탐지 예시

Wail2ban 에 의해 윈도우 방화벽에 차단 등록이 되면 아래와 같이 탐지됩니다.

로그 예시 : 필터탐지 > 시스템

[![image](/docs/images/Additianal/wail/2.png){: width="800" }](/docs/images/Additianal/wail/2.png){: target="_blank"}



 