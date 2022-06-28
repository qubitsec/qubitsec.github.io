---
title: 설정
permalink: defense_setting_waf.html
sidebar: M_WAF
topnav: topnav
---

     실시간으로 해킹 로그를 탐지하여 공격자로부터 방어를 할 수 있게 설정하는 페이지입니다.
     방어 > 설정 > 웹방화벽에서 계정탈취 차단 / 계정탈취 제한 / 데이터 유출 차단 / OWASP 차단
     서비스를 이용할 수 있습니다.
     – 계정탈취, 데이터 유출 필터 사용 후 차단 서비스 가능 (단, 웹방화벽 라이센스 사용 시)

<br />
웹방화벽 설정
- 분류
    - 사용자가 방어하고자 하는 분류 유형을 선택합니다.
- 예외조건
    - 예외조건에 등록한 IP는 방어가 되지 않습니다.
- 동작
    - 방어상태의 ON/OFF로 해당 공격에 대한 방어를 실행 또는 해지합니다.
- 트레픽제한
    - 트레픽제한에 대한 설정을 할 수 있습니다.
    - 계정탈취필터에 등록된 호스트/경로 대상으로 동작합니다.
    - rate, burst 값은 관리 > 웹방화벽 > Group > 제한 > 트래픽 제한 내 설정 값과 동기화
- 시도응답인증
    - 시도응답인증에 대한 설정을 할 수 있습니다.
    - 계정탈취필터에 등록된 호스트/경로 대상으로 동작합니다.
    - 웹방화벽 설정에서 등록한 그룹이 노출됩니다.

<br />
- 계정탈취 차단

[![image](/docs/images/Manual/waf/defense/setting/1.png){: width="800" }](/docs/images/Manual/waf/defense/setting/1.png){: target="_blank"}

<br />
- 계정탈취 제한

[![image](/docs/images/Manual/waf/defense/setting/2.png){: width="800" }](/docs/images/Manual/waf/defense/setting/2.png){: target="_blank"}

<br />
- 데이터 유출 차단

[![image](/docs/images/Manual/waf/defense/setting/3.png){: width="800" }](/docs/images/Manual/waf/defense/setting/3.png){: target="_blank"}

<br />
- OWASP 차단

[![image](/docs/images/Manual/waf/defense/setting/4.png){: width="800" }](/docs/images/Manual/waf/defense/setting/4.png){: target="_blank"}
