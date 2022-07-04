---
title: 대시보드
permalink: ko_dash_board.html
sidebar: M_SIEM
topnav: topnav
---

     실시간으로 해킹 로그를 탐지하여 시각화로 보여주는 페이지입니다.
     대시보드에서 보여지는 모든 로그들은 먼저 필터페이지에서 필터등록을 해야 합니다.

<br />

대시보드 상단에서는 총 탐지건수 / 등록 시스템 / 탐지로그 발생 시스템 수 / 로그 미업로드 시스템 수 / 로그 업로드량 / 리소스모니터링을 보여줍니다.

[![image](/docs/images/Manual/siem/dash/1.png){: width="800" }](/docs/images/Manual/siem/dash/1.png){: target="_blank"}

<br />

- 해당 시스템 수를 클릭하면 시스템 관리 페이지로 이동합니다.   
[![image](/docs/images/Manual/siem/dash/2.png)](/docs/images/Manual/siem/dash/2.png){: target="_blank"}

- 1시간 이내에 로그 발생이 없는 경우, 시스로그/웹로그 미업로드 시스템 항목에 표시됩니다.

[![image](/docs/images/Manual/siem/dash/3.png){: width="800" }](/docs/images/Manual/siem/dash/3.png){: target="_blank"}

<br />

그 아래에는 마이터 어택 / 상관분석 / 데이터 유출 / 계정 탈취 / 시스템 / 응용프로그램 / 웹 / 네트워크 에서 탐지된 로그의 수를 보여줍니다.

<br />

## 1. 마이터 어택 / 상관분석 / 데이터 유출 / 계정 탈취 / 시스템 / 응용프로그램 / 웹 / 네트워크
- 해당 로그를 선택하면 아래 항목들이 보여집니다.   
[![image](/docs/images/Manual/siem/dash/4.png){: width="800" }](/docs/images/Manual/siem/dash/4.png){: target="_blank"}

- 최근 탐지된 로그
- 탐지필터 TOP 5
- 위험도별 로그발생 현황
- 시간별 로그발생 현황
- 접속 IP TOP5
- 탐지로그 서버 TOP5

<br />

- 최근 탐지된 로그의 ‘더보기’를 클릭하면 해당 탐지로그 페이지로 이동합니다.

[![image](/docs/images/Manual/siem/dash/5.png)](/docs/images/Manual/siem/dash/5.png){: target="_blank"}

<br />

[![image](/docs/images/Manual/siem/dash/6.png){: width="800" }](/docs/images/Manual/siem/dash/6.png){: target="_blank"}

<br />

## 2. 시간별 로그 발생 현황

- 전일발생 그래프와 비교하여 탐지라인 그래프를 확인할 수 있습니다.   
[![image](/docs/images/Manual/siem/dash/7.png){: width="800" }](/docs/images/Manual/siem/dash/7.png){: target="_blank"}

<br />

## 3. 화면 설정

- 대시보드 우측 톱니바퀴를 클릭하면 화면설정 페이지가 노출됩니다.   
[![image](/docs/images/Manual/siem/dash/8.png){: width="800" }](/docs/images/Manual/siem/dash/8.png){: target="_blank"}

<br />

[![image](/docs/images/Manual/siem/dash/9.png){: width="800" }](/docs/images/Manual/siem/dash/9.png){: target="_blank"}

 <br />

+ 그룹 설정
   - 대시보드에 표시할 시스템 그룹 설정
   - 상단 영역 노출
   - 상단에 노출되는 영역 설정
   - 디폴트 메뉴
   - 대시보드에 접속 시 보이는 로그
   - 메뉴 노출 설정
   - 사용자가 원하는 로그만 대시보드에 노출
   - 개인 대시보드 사용
   - 사용자 커스텀 대시보드 기능 사용 설정
   - 초기화
   - 디폴트 메뉴는 상관분석
   - 메뉴 노출 설정은 전체로 설정됩니다.

<br />

## 4. 개인 대시보드

- 사용자가 원하는 필터를 설정하여 모니터링할 수 있습니다.   
[![image](/docs/images/Manual/siem/dash/10.png){: width="800" }](/docs/images/Manual/siem/dash/10.png){: target="_blank"}   
[![image](/docs/images/Manual/siem/dash/11.png){: width="800" }](/docs/images/Manual/siem/dash/11.png){: target="_blank"}

 참고영상_PLURA V5 대시보드/메뉴 활용하기   
 [https://qubitsec.github.io/ko_dash_menu.html](https://qubitsec.github.io/ko_dash_menu.html){: target="_blank"}