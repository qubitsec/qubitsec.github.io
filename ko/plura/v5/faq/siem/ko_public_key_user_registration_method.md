---
title: 공개키 로그인 성공
permalink: ko_public_key_user_registration_method.html
sidebar: faq_siem_M
topnav: topnav
---

**PLURA V5 > 필터 > 등록 > 호스트**

[![image](/docs/images/Additianal/public_key/02.png){: width="800" }](/docs/images/Additianal/public_key/02.png){: target="_blank"}

- 운영체제 그룹 : linux
- 운영체제 : ubuntu or centos (해당되는 운영체제 선택)
- 채널 : Syslog
- 필터명 : 공개키 로그인 성공
- 필터설명 : 공개키 로그인 성공 시 발생되는 로그입니다.
- 필터위험도 : 높음
- 필터동작시간 : 24시간
- 필터상태 : ON

<br />

**기본 등록 정보**

- 정보입력 > msg > 직접입력 : Accepted publickey for > 포함

 
<br />

**내부 IP 주소 제외 처리 필요한 경우 등록 정보**

- 정보입력 > msg > 직접입력 : Accepted publickey for > 포함
- 정보입력 > msg > 선택입력 : default > 제외
- default: default 에 등록되어 있는 IP 주소 탐지 제외 처리