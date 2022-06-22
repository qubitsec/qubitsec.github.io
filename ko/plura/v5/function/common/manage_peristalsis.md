---
title: 연동
permalink: manage_peristalsis.html
sidebar: M_C
topnav: topnav
---

- 연동 : 컴플라이언스 수정 및 티켓 관리, Syslog 연동 설정을 할 수 있습니다.

 [![image](/docs/images/Manual/common/manage/peristalsis/1.png)](/docs/images/Manual/common/manage/peristalsis/1.png){: target="_blank"}

#### ◆ 컴플라이언스
– PCI-DSS_v3.2.1, ISMS-P, ISO27001:2013, 전자금융감독규정에 대한 적용 및 수정을 할 수 있습니다.
※ PLURA V5 Forensic 제품에서는 지원하지 않는 기능입니다.

#### ◆ 티켓 연동 설정
– 티켓 “수정하기” 버튼을 클릭한 후, 설정할 수 있습니다.

 [![image](/docs/images/Manual/common/manage/peristalsis/2.png)](/docs/images/Manual/common/manage/peristalsis/2.png){: target="_blank"}

– 수정 완료 후 우측 하단의 티켓 발행 테스트 버튼으로 정상 연동 여부를 확인할 수 있습니다.

 [![image](/docs/images/Manual/common/manage/peristalsis/3.png)](/docs/images/Manual/common/manage/peristalsis/3.png){: target="_blank"}

#### ◆ 티켓 발행
– 티켓 발행을 원하는 로그에서 우측 하단의 티켓 버튼을 클릭하면 티켓이 발행됩니다.

 [![image](/docs/images/Manual/common/manage/peristalsis/4.png)](/docs/images/Manual/common/manage/peristalsis/4.png){: target="_blank"}

– 티켓이 발행되면 연동한 시스템에서 내용을 확인할 수 있습니다.

 [![image](/docs/images/Manual/common/manage/peristalsis/5.png)](/docs/images/Manual/common/manage/peristalsis/5.png){: target="_blank"}

– 로그 조회 페이지 상단에 발행티켓 버튼을 클릭하면, 발행티켓 페이지로 이동하여 발행된 티켓에 대한 정보를 확인할 수 있습니다.

 [![image](/docs/images/Manual/common/manage/peristalsis/6.png)](/docs/images/Manual/common/manage/peristalsis/6.png){: target="_blank"}


#### ◆ Syslog 연동 설정

a. 대표/그룹별 선택 가능
– 대표 또는 서비스 그룹별로 구분하여 Syslog 알림을 받을 수 있습니다.

b. 알림 상세 선택

 [![image](/docs/images/Manual/common/manage/peristalsis/7.png)](/docs/images/Manual/common/manage/peristalsis/7.png){: target="_blank"}

– 추가, 삭제 버튼을 이용하여 syslog 알림을 받을 서버 편집을 할 수 있습니다.
– 편집 버튼을 클릭하면 상세 알림을 선택할 수 있는 팝업창이 노출됩니다.
▶ 탐지 : 마이터, 상관분석, 데이터유출, 계정탈취, 시스템로그, 웹로그, 네트워크로그
▶ 방어 : 상관분석, 데이터유출, 계정탈취, 시스템로그, 웹로그, 네트워크로그
▶ 사용로그 : 멤버, 필터, 서버, 방어, 고객지원, 기타

c. syslog 알림을 받고자 하는 서버의 환경 정보 입력
– 프로토콜, Syslog 포맷 형식, 서버 IP 주소, 포트번호, 개행타입을 입력합니다.
– 예시_Syslog 설정

 [![image](/docs/images/Manual/common/manage/peristalsis/8.png)](/docs/images/Manual/common/manage/peristalsis/8.png){: target="_blank"}
