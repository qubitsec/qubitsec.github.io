---
title: Syslog 설정으로 kiwi에서 받기
permalink: ko_send_syslog_kiwi.html
sidebar: faq_siem_M
topnav: topnav
---

<br />

## 1. Kiwi 다운로드 및 설치

 다운로드 URL: [https://www.kiwisyslog.com/free-tools/kiwi-free-syslog-server](https://www.kiwisyslog.com/free-tools/kiwi-free-syslog-server){: target="_blank"}

 [![image](/docs/images/Faq/kiwi/05.png){: width="800" }](/docs/images/Faq/kiwi/05.png){: target="_blank"}

<br /> 

## 2. Kiwi Syslog 실행

설치한 Kiwi Syslog 를 실행하면, 아래와 같은 화면이 노출됩니다.

 [![image](/docs/images/Faq/kiwi/01.png){: width="800" }](/docs/images/Faq/kiwi/01.png){: target="_blank"}

<br />

## 3. 단축키 실행

프로그램 상단 "File" → "Setup" 또는 "Ctrl+P" 단축키를 실행합니다.

 [![image](/docs/images/Faq/kiwi/02.png){: width="800" }](/docs/images/Faq/kiwi/02.png){: target="_blank"}

<br />

## 4. Source IP Address 추가

Inputs 옵션 → Source IP Address를 추가합니다.

 [![image](/docs/images/Faq/kiwi/03.png){: width="800" }](/docs/images/Faq/kiwi/03.png){: target="_blank"}

<br />

## 5. 설정 추가

### 5-1. [송신] PLURA 설정

PLURA 페이지 좌측 상단 관리 > 연동 메뉴에서 다음과 같이 설정하실 수 있습니다.

[그룹알림-syslog 연동설정](https://qubitsec.github.io/ko_manage_peristalsis.html#4-syslog-%EC%97%B0%EB%8F%99-%EC%84%A4%EC%A0%95){: target="_blank"}

  - 수신지 IP주소를 입력
 
 <br />
 
### 5-2. [수신] Kiwi Syslog 설정

  - Kiwi Memu > File > Setup > Inputs > UDP > Data encoding : UTF-8 설정
  - Kiwi Memu > File > Setup > Inputs > IP addresses 메뉴에 송신지 IP주소 Add
     - 송신지 IP주소는 고객사마다 다릅니다.
 






 