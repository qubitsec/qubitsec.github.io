---
title: 백신 소프트웨어 종료 탐지 방법
permalink: antivirus_sw.html
sidebar: faq_siem_M
topnav: topnav
---

## 1. Windows Defender 종료 탐지

**필터명 “Windows Defender 종료”로 기본 제공.**
 
<br />

## 2. 기타 백신 소프트웨어 종료 탐지

**웹에서 필터 등록으로 설정 방법**

2-1. 필터 > 등록 선택

<br />

2-2. 서버그룹 선택 > 운영체제 Windows 선택 > Security 채널 선택 > 세부 추적 분류 선택 > 이벤트타입 선택


[![image](/docs/images/Additianal/anti/1.png){: width="800" }](/docs/images/Additianal/anti/1.png){: target="_blank"}
 
<br />

이벤트 타입에서 프로세스 종료(4689) 선택

[![image](/docs/images/Additianal/anti/2.png)](/docs/images/Additianal/anti/2.png){: target="_blank"}

그림과 같이 선택 후 ‘데이터 값’에 사용하는 백신의 필수 프로세스명을 넣고 하단의 ‘등록’ 버튼 클릭

<br />

**예시 Alyac**
[![image](/docs/images/Additianal/anti/3.png){: width="800" }](/docs/images/Additianal/anti/3.png){: target="_blank"}

<br />

`# C:\Program Files\ESTsoft\ALYac\AYRTSrv.aye`

<br />

**예시 V3**
[![image](/docs/images/Additianal/anti/4.png){: width="800" }](/docs/images/Additianal/anti/4.png){: target="_blank"}

<br />

`# C:\Program Files\AhnLab\V3*\ASDSvc.exe`

<br />

**예시 Kaspersky**

[![image](/docs/images/Additianal/anti/5.png)](/docs/images/Additianal/anti/5.png){: target="_blank"}

<br />

`# C:\Program Files*\Kaspersky Lab\*\avp.exe`

<br />

**예시 Symantec Norton**

[![image](/docs/images/Additianal/anti/6.png){: width="800" }](/docs/images/Additianal/anti/6.png){: target="_blank"}

<br />

`# C:\Program Files\Norton Security\Engine\*\NortonSecurity.exe`