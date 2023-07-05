---
title: 연동
permalink: ko_manage_peristalsis.html
sidebar: M_C
topnav: topnav
---

- 연동 : 컴플라이언스 수정 및 티켓 관리, Syslog 연동 설정을 할 수 있습니다.

 [![image](/docs/images/Manual/common/manage/peristalsis/9.png){: width="800" }](/docs/images/Manual/common/manage/peristalsis/9.png){: target="_blank"}

 <br />

## 1. 컴플라이언스
- PCI-DSS_v3.2.1, ISMS-P, ISO27001:2013, 전자금융감독규정에 대한 적용 및 수정을 할 수 있습니다.   
- PLURA V5 Forensic 제품에서는 지원하지 않는 기능입니다.

<br />

## 2. 티켓 연동 설정

- 티켓 “수정하기” 버튼을 클릭한 후, 설정할 수 있습니다.   
 [![image](/docs/images/Manual/common/manage/peristalsis/2.png){: width="800" }](/docs/images/Manual/common/manage/peristalsis/2.png){: target="_blank"}

<br />

- 수정 완료 후 우측 하단의 티켓 발행 테스트 버튼으로 정상 연동 여부를 확인할 수 있습니다.   
 [![image](/docs/images/Manual/common/manage/peristalsis/3.png){: width="800" }](/docs/images/Manual/common/manage/peristalsis/3.png){: target="_blank"}

<br />

## 3. 티켓 발행

- 티켓 발행을 원하는 로그에서 우측 하단의 티켓 버튼을 클릭하면 티켓이 발행됩니다.   
 [![image](/docs/images/Manual/common/manage/peristalsis/4.png){: width="800" }](/docs/images/Manual/common/manage/peristalsis/4.png){: target="_blank"}

<br />

- 티켓이 발행되면 연동한 시스템에서 내용을 확인할 수 있습니다.   
 [![image](/docs/images/Manual/common/manage/peristalsis/5.png){: width="800" }](/docs/images/Manual/common/manage/peristalsis/5.png){: target="_blank"}

- 로그 조회 페이지 상단에 발행티켓 버튼을 클릭하면, 발행티켓 페이지로 이동하여 발행된 티켓에 대한 정보를 확인할 수 있습니다.   
 [![image](/docs/images/Manual/common/manage/peristalsis/6.png){: width="800" }](/docs/images/Manual/common/manage/peristalsis/6.png){: target="_blank"}

<br />

## 4. Syslog 연동 설정

4-1. 대표/그룹별 선택 가능
- 대표 또는 서비스 그룹별로 구분하여 Syslog 알림을 받을 수 있습니다.

<br />

4-2. 알림 상세 선택   
 [![image](/docs/images/Manual/common/manage/peristalsis/14.png){: width="800" }](/docs/images/Manual/common/manage/peristalsis/14.png){: target="_blank"}

- 추가, 삭제 버튼을 이용하여 Syslog 알림을 받을 서버 편집을 할 수 있습니다.
- 탭 이동(탐지, 방어, 사용로그)을 하여 설정을 변경할 수 있습니다.
- 편집 버튼을 클릭하면 상세 알림을 선택할 수 있는 팝업창이 노출됩니다.
   - 탐지 : 상관분석, 호스트, 웹, 네트워크, 계정탈취, 데이터 유출, 마이터 어택, 웹방화벽, 응용프로그램, 호스트보안
   - 방어 : 상관분석, 호스트, 웹, 네트워크, 계정탈취, 데이터 유출, 웹방화벽, 호스트보안
   - 사용로그 : 멤버, 필터, 호스트, 방어, 고객지원, 기타

<br />

4-3. Syslog 알림을 받고자 하는 서버의 환경 정보 입력
- 프로토콜, Syslog 포맷, 서버 IP 주소, 포트번호, 개행타입을 입력합니다.
   - Syslog 포맷 : RFC3164, RFC5424, CEF 지원   
   ※ CEF : ArcSight CEF 포맷임.

- 예시_Syslog 설정

 [![image](/docs/images/Manual/common/manage/peristalsis/13.png){: width="800" }](/docs/images/Manual/common/manage/peristalsis/13.png){: target="_blank"}
###