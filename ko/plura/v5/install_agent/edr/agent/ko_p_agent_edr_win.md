---
title: Windows
permalink: ko_p_agent_edr_win.html
sidebar: Install_A_E
product: Install_A_E
---

<br />

호스트보안 Windows Agent 설치방법입니다. 순서대로 진행해 주세요.


      제조사가 지원을 종료한 제품에 대하여 PLURA V5에서도 지원을 종료합니다.
      PLURA V5에서 지원하지 않는 운영체제 버전을 사용한다면 문제가 발생할 수 있습니다.
      제조사가 지원 종료한 버전을 사용 중이라면 업그레이드에 대하여 보다 적극적인 검토가 필요합니다.
      해킹과 장애 등 다양한 문제에 직면하고 심각한 문제로 발전할 수 있기 때문입니다.

## 설치 안내

<!-- 샘플 : __1.1 파일 다운로드__ -->

### 1. 파일 다운로드

먼저 아래 링크를 클릭하여 호스트보안 에이전트 설치 파일을 다운로드 합니다.   

[다운로드](https://repo.plura.io/v5/agent/win/PluraSetup.exe)

<br />

### 2. 설치 시작

[![image](/docs/images/Ins_G/Agent_W/Agent_W_1.png)](/docs/images/Ins_G/Agent_W/Agent_W_1.png){:target="_blank"}

<br />

### 3. 설치 경로 선택

[![image](/docs/images/Ins_G/Ins_EDR/006.png)](/docs/images/Ins_G/Ins_EDR/006.png){:target="_blank"}

<br />

### 4. 로그인

(1) 설치가 완료되면 로그인 창이 자동 실행 됩니다.

(2) 웹페이지에서 확인한 라이센스를 입력합니다.

[![image](/docs/images/Ins_G/Agent_W/Agent_W_3.png)](/docs/images/Ins_G/Agent_W/Agent_W_3.png){:target="_blank"}

<br />

### 5. 서비스 시작

(1) 로그인 되면 PLURA V5 서비스가 시작됩니다.

(2) 마지막 로그 업로드 시간이 보인다면 로그가 정상적으로 업로드 되고있는 것입니다.

[![image](/docs/images/Ins_G/Agent_W/Agent_W_4.png)](/docs/images/Ins_G/Agent_W/Agent_W_4.png){:target="_blank"}

<br />

### 6. Sysmon 설치

(1) Sysmon 다운로드

- 최신버전 다운로드 링크 : [ Sysmon ](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon){:target="_blank"}

<br />

(2) 설치

- 관리자 권한으로 cmd 실행하여 Sysmon.exe 파일의 경로로 이동

- 아래 명령어 실행   
`sysmon.exe -accepteula -i “C:\Program Files\PLURA\sysmon-plura.xml”`

<br />

(3) 확인

Agent 에서 Sysmon 설치 확인

[![image](/docs/images/Ins_G/Sysmon/sysmon_3.png)](/docs/images/Ins_G/Sysmon/sysmon_3.png){:target="_blank"}

<br />

### 7. 서비스 중지

(1) 활성화 되어있는 ‘에이전트 상태’ 버튼을 누르면 PLURA V5 서비스가 중지됩니다.

[![image](/docs/images/Ins_G/Agent_W/Agent_W_5.png)](/docs/images/Ins_G/Agent_W/Agent_W_5.png){:target="_blank"}

[![image](/docs/images/Ins_G/Agent_W/Agent_W_6.png)](/docs/images/Ins_G/Agent_W/Agent_W_6.png){:target="_blank"}

<br />

### 8. 웹 로그 수집 설정

웹 로그를 수집하는 기능을 추가하는 내용입니다.
웹 로그 취합을 진행하시려면 아래 내용대로 따라해 주세요.

(1) <font color='dodgerblue'> www.plura.io </font> 에 접속하여 해당 시스템의 웹 로그 수집 기능을 활성화 시킵니다.

* 시스템 > 시스템 관리에 들어갑니다.

* 시스템 목록 중 사용자의 시스템 IP 주소에 해당하는 목록을 클릭합니다.

(2-1) 웹로그 수집 ON 후 수정 버튼을 클릭합니다. 해제를 원하시면 OFF 합니다.

[![image](/docs/images/Ins_G/Ins_EDR/005.png){: width="800" }](/docs/images/Ins_G/Ins_EDR/005.png){:target="_blank"}

(2-2) 또는 에이전트의 웹로그 설정 메뉴에서 웹로그 수집 체크를 합니다. 해제를 원하시면 언체크 합니다.

[![image](/docs/images/Ins_G/Ins_EDR/001.png)](/docs/images/Ins_G/Ins_EDR/001.png){:target="_blank"}

<br />

<!--
## Step 3

__자동 업데이트 기능__

PLURA V5 Agent 자동 업데이트 기능을 사용하시려면 환경설정 탭으로 이동하여 자동업데이트 체크박스에 체크 되어있는지 확인합니다. 기본값은 체크 상태입니다.

[![image](/docs/images/Ins_G/Ins_EDR/002.png)](/docs/images/Ins_G/Ins_EDR/002.png){:target="_blank"}

<br />



## Step 4

__업데이트 확인__

PLURA V5 Agent의 업데이트 버전은 C:\Program Files\PLURA 경로에서 확인 하실 수 있습니다.

**ex)PLURAService 버전 확인**

[![image](/docs/images/Ins_G/Ins_EDR/003.png){: width="800" }](/docs/images/Ins_G/Ins_EDR/003.png){:target="_blank"}

<br />

[![image](/docs/images/Ins_G/Ins_EDR/004.png)](/docs/images/Ins_G/Ins_EDR/004.png){:target="_blank"}

<br />

-->


<!-- 주석 Sample
-->



<!--
######### 삭제된 내용
## Windows Agent 설치 영상

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/kKLL_sP9w9c' frameborder='0' allowfullscreen></iframe></div>

## 웹로그 수집 설정 영상
<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/kKLL_sP9w9c' frameborder='0' allowfullscreen></iframe></div>
-->

