---
title: 홈페이지 위변조
permalink: s_f_h_forgery.html
sidebar: M_C
topnav: topnav
---

PLURA V5의 보안필터 중 홈페이지 위변조는 등록된 홈페이지 파일명이나 파일의 내용이 변경되는 것을 탐지하는 필터입니다.

<br />
[![image](/docs/images/Manual/common/filter2/security/forgery/1.png){: width="800" }](/docs/images/Manual/common/filter2/security/forgery/1.png){: target="_blank"}

홈페이지 위변조는 운영체제(Windows, CentOS)별 필터 등록이 가능합니다.

아래는 등록 예시입니다. (시스템 IP를 제외한 전체 경로 입력)

<br />
[![image](/docs/images/Manual/common/filter2/security/forgery/2.png){: width="800" }](/docs/images/Manual/common/filter2/security/forgery/2.png){: target="_blank"}

<br />
※ 아래 참고 이미지처럼 type=SYSCALL로 노출되는 경우, 변조된 파일 경로까지는 확인할 수 없습니다.
(OS 버전별로 차이가 있을 수 있습니다.)

<br />
[![image](/docs/images/Manual/common/filter2/security/forgery/3.png){: width="800" }](/docs/images/Manual/common/filter2/security/forgery/3.png){: target="_blank"}

