---
title: 에이전트 삭제
permalink: ko_agent_uninstall.html
sidebar: faq_common_M
topnav: topnav
---

<br />

### 1. Window 에이전트

<br />

#### 1-1. 경로 이동

 ‘제어판 > 프로그램 > 프로그램 및 기능 > 프로그램 제거 또는 변경’ 으로 이동합니다.

<br />

#### 1-2. PLURA 제거/변경 클릭

[![image](/docs/images/Faq/Agent/03.png)](/docs/images/Faq/Agent/03.png){: target="_blank"}

<br />

#### 1-3. PLURA 삭제 

PLURA 제거 팝업이 뜨고 ‘예’를 클릭합니다.

[![image](/docs/images/Faq/Agent/04.png)](/docs/images/Faq/Agent/04.png){: target="_blank"}

<br />

#### 1-4. 웹로그 모듈 삭제

웹로그 수집을 해지한 뒤, 웹로그 모듈을 삭제하려는 사용자인 경우 ‘웹로그 설정 > 웹로그 모듈 삭제’ 버튼을 통해 삭제하시면 됩니다.

[![image](/docs/images/Faq/Agent/05.png)](/docs/images/Faq/Agent/05.png){: target="_blank"}

<br />

### 2. Linux 에이전트

리눅스에서 PLURA V5 Agent 삭제 방법입니다.

아래 Command 를 실행하시면 PLURA V5 Agent 관련 모든 모듈이 삭제됩니다.

<br />

#### 2-1. CentOS/RHEL/Ubuntu Agent 삭제

``# /etc/plura/plura.sh uninstall``
