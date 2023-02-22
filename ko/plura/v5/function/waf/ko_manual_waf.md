---
title: 대시보드
permalink: ko_manual_waf.html
sidebar: M_WAF
topnav: topnav
---


     실시간으로 해킹 로그를 탐지하여 시각화로 보여주는 페이지입니다.
     대시보드에서 보여지는 모든 로그들은 먼저 필터페이지에서 필터등록을 해야 합니다.

<br />

대시보드에서는 오늘 탐지된 로그를 시간별로 설정하여 조회가 가능합니다.   
※시간 단위로만 조회가 가능합니다.

[![image](/docs/images/Manual/siem/dash/13.png){: width="500" }](/docs/images/Manual/siem/dash/13.png){: target="_blank"}

<br />

대시보드 상단에서는 총 탐지건수 / 등록 시스템 / 탐지로그 발생 시스템 수 / 로그 미업로드 시스템 수 / 로그 업로드량 / 리소스모니터링을 보여줍니다.

[![image](/docs/images/Manual/siem/dash/1.png){: width="800" }](/docs/images/Manual/siem/dash/1.png){: target="_blank"}

<br />

그 아래에는 웹방화벽에서 탐지된 로그의 수를 보여줍니다.

## 1. 실시간 탐지 항목

- Status별, 차단/탐지별 조회가 가능합니다.

[![image](/docs/images/Manual/waf/manual/07.png){: width="800" }](/docs/images/Manual/waf/manual/07.png){: target="_blank"}

- 최근 탐지된 로그
- 탐지필터 TOP 5
- Status별 로그발생 현황
- 시간별 로그발생 현황
- 접속 IP TOP5
- 탐지로그 시스템 TOP5

<br />

- 최근 탐지된 로그의 ‘더보기’를 클릭하면 해당 탐지로그 페이지로 이동합니다.

[![image](/docs/images/Manual/waf/manual/02.png)](/docs/images/Manual/waf/manual/02.png){: target="_blank"}

<br />

## 2. 탐지필터 TOP5 / 위험도별 로그발생 현황

- 탐지필터 TOP5와 위험도별 로그발생 현황 그래프를 확인할 수 있습니다.   
[![image](/docs/images/Manual/waf/manual/05.png){: width="800" }](/docs/images/Manual/waf/manual/05.png){: target="_blank"}

<br />

## 3. 시간별 로그 발생 현황

- 전일발생 그래프와 비교하여 탐지라인 그래프를 확인할 수 있습니다.   
[![image](/docs/images/Manual/waf/manual/04.png){: width="800" }](/docs/images/Manual/waf/manual/04.png){: target="_blank"}

<br />

## 4. 접속 IP TOP5 / 탐지로그 시스템 TOP5

- 접속 IP TOP5와 탐지로그 시스템 TOP5 현황을 확인할 수 있습니다.   
[![image](/docs/images/Manual/waf/manual/06.png){: width="800" }](/docs/images/Manual/waf/manual/06.png){: target="_blank"}