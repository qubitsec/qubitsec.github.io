---
title: 관리 > 웹방화벽
permalink: ko_web_firewall_waf.html
sidebar: M_WAF
topnav: topnav
---

<br />

- 시스템 그룹 별로 웹방화벽 설정을 진행할 수 있습니다.   
 [![image](/docs/images/Manual/waf/firewall/1.png){: width="800" }](/docs/images/Manual/waf/firewall/1.png){: target="_blank"}

<br />

- “그룹추가” 버튼을 클릭하여, 시스템 그룹을 추가할 수 있습니다.   
 [![image](/docs/images/Manual/waf/firewall/2.png)](/docs/images/Manual/waf/firewall/2.png){: target="_blank"}

<br />

- 시스템 그룹 별로 웹방화벽 공지 설정을 진행할 수 있습니다.   
  - 접속예외 설정을 통해 점검 중 예외처리(IP주소 등록)가 가능합니다.

  [![image](/docs/images/Manual/waf/firewall/9.png){: width="800" }](/docs/images/Manual/waf/firewall/9.png){: target="_blank"}

<br />

- 웹방화벽 공지 설정 > 미리보기 버튼을 클릭하여 작성한 내용을 확인할 수 있습니다.
 [![image](/docs/images/Manual/waf/firewall/10.png){: width="800" }](/docs/images/Manual/waf/firewall/10.png){: target="_blank"}

<br />

- 시스템 그룹 별로 웹방화벽 차단 안내 설정을 진행할 수 있습니다.   
 [![image](/docs/images/Manual/waf/firewall/11.png){: width="800" }](/docs/images/Manual/waf/firewall/11.png){: target="_blank"}

<br />

- 다음은 차단 안내 화면 예시입니다.
 [![image](/docs/images/Manual/waf/firewall/12.png){: width="800" }](/docs/images/Manual/waf/firewall/12.png){: target="_blank"}

<br />

- 운영방식 : 해당 그룹의 웹방화벽 운영방식을 탐지/차단 중 설정할 수 있습니다.   
 [![image](/docs/images/Manual/waf/firewall/3.png)](/docs/images/Manual/waf/firewall/3.png){: target="_blank"}

<br />

- X-Forwarded-For : 입력/출력을 설정할 수 있습니다.   
 [![image](/docs/images/Manual/waf/firewall/4.png)](/docs/images/Manual/waf/firewall/4.png){: target="_blank"}

<br />

- Proxy : Proxy 설정(웹방화벽 SSL, 호스트 등)을 할 수 있습니다.

<br />

- “호스트” 불러오기 : 관리 > 목록 > 호스트에 등록한 정보를 가져올 수 있습니다.   
 [![image](/docs/images/Manual/waf/firewall/5.png){: width="800" }](/docs/images/Manual/waf/firewall/5.png){: target="_blank"}
 
<br />

- 접근제한 ON 하는 경우, IP주소와 GeoIP 설정을 관리자가 직접 설정할 수 있습니다.   

- GeoIP의 경우, 체크박스를 선택한 국가에서만 접근(Whitelist)이 가능합니다.   
  [![image](/docs/images/Manual/waf/firewall/6.png){: width="800" }](/docs/images/Manual/waf/firewall/6.png){: target="_blank"}

<br />

- 접근제한 > IP주소 > “등록” 버튼을 클릭하면 특정 IP 접속에 대한 허용/차단 설정을 할 수 있습니다.   
  [![image](/docs/images/Manual/waf/firewall/7.png)](/docs/images/Manual/waf/firewall/7.png){: target="_blank"}

<br />

- 제한 : 트래픽 제한, 시도응답인증, 일정 변경을 통해 웹방화벽에 대한 제한 설정을 할 수 있습니다.   

- 계정탈취필터에 등록된 호스트/경로가 있어야 설정할 수 있습니다.   
 [![image](/docs/images/Manual/waf/firewall/8.png){: width="800" }](/docs/images/Manual/waf/firewall/8.png){: target="_blank"}

<br />

 - 관리 > 사용 메뉴에서 PLURA 웹방화벽의 탐지/차단 예외를 설정할 수 있습니다.
 [https://qubitsec.github.io/ko_manage_use.html](https://qubitsec.github.io/ko_manage_use.html){: target="_blank"}