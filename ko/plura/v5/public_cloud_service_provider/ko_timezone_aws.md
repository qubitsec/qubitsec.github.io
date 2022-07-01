---
title: AWS에서 타임존 설정
permalink: ko_timezone_aws.html
sidebar: PCSP
topnav: topnav
---

모든 로깅 시스템에서 가장 중요한 것은 시간 동기화입니다.

AWS 에서는 Local Time 기본값으로 “GMT” 가 설정됩니다.

<br />

## 1. Localtime 을 Asia/seoul 로 시간 설정 변경하는 방법

`# ln -sf /usr/share/zoneinfo/Asia/Seoul /etc/localtime`

<br />

## 2. rsyslog 를 재시작 해줘야 취합로그 시간이 변경 적용됩니다.

`# service rsyslog restart`

<br />

**시나리오1_현재 Local time 확인**

`# date`
[![image](/docs/images/Public_Cloud/timezone/01.png){: width="800" }](/docs/images/Public_Cloud/timezone/01.png){: target="_blank"}  

Localtime 이 Mon Jul 6 02:16:00 UTC 2020 설정되어 있습니다.

<br />

**시나리오2_현재 Local time 을 Asia/seoul 로 설정 변경**

`# ln -sf /usr/share/zoneinfo/Asia/Seoul /etc/localtime`
[![image](/docs/images/Public_Cloud/timezone/02.png){: width="800" }](/docs/images/Public_Cloud/timezone/02.png){: target="_blank"}

Localtime 이 Mon Jul 6 11:16:42 KST 2020 로 변경되었습니다.

<br />

**시나리오3_rsyslog 재시작**

`# service rsyslog restart`

<br />

**시나리오 결과, Localtime 이 변경되었습니다.**

(기존) Mon Jul 6 02:16:00 UTC 2020  

→ (변경) Mon Jul 6 11:16:42 KST 2020

<br />

## 3. PLURA V5 페이지의 시간설정 방법

PLURA V5 > 관리 > 시스템 > 시간

Windows 서버의 경우, UTC 기준으로 시간이 설정되어 아래와 같이 Localtime 을 설정해주어야 합니다.