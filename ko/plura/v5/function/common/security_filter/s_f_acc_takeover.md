---
title: 계정탈취
permalink: s_f_acc_takeover.html
sidebar: M_C
topnav: topnav
---

     계정탈취 보안필터에는 크리덴셜 스터핑, 볼륨 메트릭이 있습니다.

<br />
▶ 크리덴셜 스터핑이란?
[https://owasp.org/www-community/attacks/Credential_stuffing](https://owasp.org/www-community/attacks/Credential_stuffing){: target="_blank"}

PLURA V5의 보안필터 중 크리덴셜 스터핑은 꾸준한 로그인 시도를 통해 계정을 탈취하는 공격을 탐지하는 필터입니다.

▶ 볼륨 메트릭이란?
[https://www.a10networks.com/blog/understanding-ddos-attacks/](https://www.a10networks.com/blog/understanding-ddos-attacks/){: target="_blank"}

<br />
PLURA V5의 보안필터 중 볼륨 메트릭은 무자비 대입을 통해 계정을 탈취하는 공격을 탐지하는 필터입니다.

[![image](/docs/images/Manual/common/filter2/security/takeover/1.png){: width="800" }](/docs/images/Manual/common/filter2/security/takeover/1.png){: target="_blank"}

- 분류 : 볼륨 메트릭(고정), 볼륨 메트릭(가변), 크리덴셜 스터핑(고정), 크리덴셜 스터핑(가변) 중 선택할 수 있습니다.
- 필터명 : 필터명을 입력합니다. 탐지로그에 노출되는 정보로 쉽게 알아볼 수 있는 이름으로 정합니다.
- 호스트 : 호스트 정보를 입력합니다.
- 멀티 호스트 등록이 가능합니다.
- 호스트 등록은 관리 > 목록 > 호스트 메뉴에서 관리자가 등록할 수 있습니다.
(운영자, 모니터링 권한에서는 호스트 메뉴 숨김(Hidden)처리)
- 경로 : 경로(로그인 페이지)를 입력합니다.
- 메소드(Method) : POST, GET 중 선택합니다.
- 로그인 속성 : name 을 입력합니다.
- 시간대 : 설정한 시간에 필터가 동작합니다.
- 동작 : 필터 사용 유무를 선택합니다.
- Login 성공/실패 : Login 성공/실패를 선택합니다.
- 상태값 : Status를 선택합니다.
- 응답크기 : 응답크기는 상태값 표기를 위한 조건으로, PLURA V5에서 수집된 전체로그 정보를 통하여 응답크기를 확인하여 입력합니다.
응답크기를 제외하고 싶은 경우, 응답크기 체크박스를 해제합니다.
- 시도횟수/조건/사용ID수 : 탐지 조건(시도횟수/조건/사용ID수)을 입력합니다.
AND, OR 조건을 활용할 수 있습니다.

<br />
※ 예시_계정탈취 보안필터

[![image](/docs/images/Manual/common/filter2/security/takeover/2.png){: width="800" }](/docs/images/Manual/common/filter2/security/takeover/2.png){: target="_blank"}