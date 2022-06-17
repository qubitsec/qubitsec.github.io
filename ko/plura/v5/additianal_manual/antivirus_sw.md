---
title: 백신 소프트웨어 종료 탐지 방법
permalink: antivirus_sw.html
sidebar: Add_M
topnav: topnav
---

#### 1. Windows Defender 종료 탐지

- **필터명 “Windows Defender 종료”로 기본 제공.**
 

#### 2. 기타 백신 소프트웨어 종료 탐지

웹에서 필터 등록으로 설정 방법

- **필터 > 등록 선택**
- **서버그룹 선택 > 운영체제 Windows 선택 > Security 채널 선택 > 세부 추적 분류 선택 > 이벤트타입 선택**


[![image](/docs/images/Additianal/anti/1.png)](/docs/images/Additianal/anti/1.png){: target="_blank"}
 

이벤트 타입에서 프로세스 종료(4689) 선택

[![image](/docs/images/Additianal/anti/2.png)](/docs/images/Additianal/anti/2.png){: target="_blank"}

그림과 같이 선택 후 ‘데이터 값’에 사용하는 백신의 필수 프로세스명을 넣고 하단의 ‘등록’ 버튼 클릭


**예시 1) Alyac**

[![image](/docs/images/Additianal/anti/3.png)](/docs/images/Additianal/anti/3.png){: target="_blank"}




     C:\Program Files\ESTsoft\ALYac\AYRTSrv.aye

**예시 2) V3**
[![image](/docs/images/Additianal/anti/4.png)](/docs/images/Additianal/anti/4.png){: target="_blank"}




     C:\Program Files\AhnLab\V3*\ASDSvc.exe

**예시 3) Kaspersky**
[![image](/docs/images/Additianal/anti/5.png)](/docs/images/Additianal/anti/5.png){: target="_blank"}


     C:\Program Files*\Kaspersky Lab\*\avp.exe

**예시 4) Symantec Norton**
[![image](/docs/images/Additianal/anti/6.png)](/docs/images/Additianal/anti/6.png){: target="_blank"}



     C:\Program Files\Norton Security\Engine\*\NortonSecurity.exe