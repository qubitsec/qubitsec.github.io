---
title: Windows Server
permalink: p_agent_win_srv.html
sidebar: Install_A_S
product: Install_A_S
---







<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/kKLL_sP9w9c' frameborder='0' allowfullscreen></iframe></div>

<br />

Windows Server Agent 설치방법입니다. 순서대로 진행해 주세요


      제조사가 지원을 종료한 제품에 대하여 PLURA V5에서도 지원을 종료합니다.
      PLURA V5에서 지원하지 않는 운영체제 버전을 사용한다면 문제가 발생할 수 있습니다.
      제조사가 지원 종료한 버전을 사용 중이라면 업그레이드에 대하여 보다 적극적인 검토가 필요합니다.
      해킹과 장애 등 다양한 문제에 직면하고 심각한 문제로 발전할 수 있기 때문입니다.

## Step 1

PLURA V5 Agent 는 Microsoft .NET Framework 3.5 이상이 설치된 환경에서 사용 가능합니다.
Windows Server 2012 부터 기본 설치되어 있습니다.

<br />

## Step 2

먼저 해당 시스템에서 <font color='dodgerblue'> www.plura.io </font> 로그인 후 우측상단 <font color='dodgerblue'> Install Agents </font> 를 클릭하여 다운로드합니다.

__2.1 설치를 시작합니다.__

Administrator 계정으로 설치해야 합니다.

[![image](/docs/images/Ins_G/Agent_W/Agent_W_1.png)](/docs/images/Ins_G/Agent_W/Agent_W_1.png){:target="_blank"}

설치 경로를 선택할 수 있습니다.

[![image](/docs/images/Ins_G/Agent_W/Agent_W_2.png)](/docs/images/Ins_G/Agent_W/Agent_W_2.png){:target="_blank"}

<br />

__2.2 로그인 하기.__

(1) 설치가 완료되면 로그인 창이 자동 실행 됩니다.

(2) 웹페이지에서 확인한 라이센스를 입력합니다.

[![image](/docs/images/Ins_G/Agent_W/Agent_W_3.png)](/docs/images/Ins_G/Agent_W/Agent_W_3.png){:target="_blank"}

<br />

__2.3 서비스 시작__

(1) 로그인 되면 PLURA V5 서비스가 시작됩니다.

(2) 마지막 로그 업로드 시간이 보인다면 로그가 정상적으로 업로드 되고있는 것입니다.

[![image](/docs/images/Ins_G/Agent_W/Agent_W_4.png)](/docs/images/Ins_G/Agent_W/Agent_W_4.png){:target="_blank"}

<br />

__2.4 서비스 중지__

(1) 활성화 되어있는 ‘에이전트 상태’ 버튼을 누르면 PLURA V5 서비스가 중지됩니다.

[![image](/docs/images/Ins_G/Agent_W/Agent_W_5.png)](/docs/images/Ins_G/Agent_W/Agent_W_5.png){:target="_blank"}

[![image](/docs/images/Ins_G/Agent_W/Agent_W_6.png)](/docs/images/Ins_G/Agent_W/Agent_W_6.png){:target="_blank"}

<br />

## Step 3
__3.1 IIS 서버 웹 로그 사용법__

Step 2 까지는 ‘시스템 로그’ 수집에 대한 내용이며, Step 3은 ‘웹 서버 로그’를 수집하는 기능을 추가하는 내용입니다.
‘시스템 로그’만을 필요로 하신다면 이번 스텝은 진행하실 필요가 없습니다.
웹 로그 취합을 진행하시려면 아래 내용대로 따라해 주세요.

(1) <font color='dodgerblue'> www.plura.io </font> 에 접속하여 해당 시스템의 웹 로그 수집 기능을 활성화 시킵니다.

* 시스템 > 시스템 관리에 들어갑니다.

* 시스템 목록 중 사용자의 시스템 IP 주소에 해당하는 목록을 클릭합니다.

(2-1) 웹로그 수집에 체크 후 확인 버튼을 클릭합니다. 해제를 원하시면 언체크 합니다.

[![image](/docs/images/Ins_G/Agent_W/Agent_W_7.png){: width="800" }](/docs/images/Ins_G/Agent_W/Agent_W_7.png){:target="_blank"}

(2-2) 또는 에이전트의 웹로그 설정 메뉴에서 웹로그 수집 체크를 합니다. 해제를 원하시면 언체크 합니다.

[![image](/docs/images/Ins_G/Agent_W/Agent_W_8.png)](/docs/images/Ins_G/Agent_W/Agent_W_8.png){:target="_blank"}

<br />

(3) 잠시 기다리시면 __[Visual C++ 재배포 가능 패키지]__ 설치 알림 창이 뜨게 됩니다.

[확인]을 누르시어, 두 번째 하단의 이미지와 같이 재배포 가능 패키지를 설치하시면 웹 로그 취합기능을 정상적으로 사용하실 수 있습니다.

[![image](/docs/images/Ins_G/Agent_W/Agent_W_9.png)](/docs/images/Ins_G/Agent_W/Agent_W_9.png){:target="_blank"}

수동 다운로드 링크 : [Visual Studio 2012 Visual C++ 재배포 가능 패키지](https://download.microsoft.com/download/1/6/B/16B06F60-3B20-4FF2-B699-5E9B7962F9AE/VSU_4/vcredist_x64.exe){:target="_blank"}

수동 다운로드 링크 : [Visual Studio 2013 Visual C++ 재배포 가능 패키지](https://download.microsoft.com/download/2/E/6/2E61CFA4-993B-4DD4-91DA-3737CD5CD6E3/vcredist_x64.exe){:target="_blank"}



## Step 4

__4.1 자동 업데이트 기능__

PLURA V5 Agent 자동 업데이트 기능을 사용하시려면
환경설정 탭으로 이동하여 자동업데이트 체크박스에 체크 되어있는지 확인합니다. 기본값은 체크 상태입니다.

[![image](/docs/images/Ins_G/Agent_W/Agent_W_10.png)](/docs/images/Ins_G/Agent_W/Agent_W_10.png){:target="_blank"}

<br />

## Step 5

__5.1 업데이트 확인__

PLURA V5 Agent의 업데이트 버전은
C:\Program Files (x86)\PLURA 경로에서 확인 하실 수 있습니다.


**ex)PLURAService 버전 확인**

[![image](/docs/images/Ins_G/Agent_W/Agent_W_11.png){: width="800" }](/docs/images/Ins_G/Agent_W/Agent_W_11.png){:target="_blank"}

<br />

[![image](/docs/images/Ins_G/Agent_W/Agent_W_12.png)](/docs/images/Ins_G/Agent_W/Agent_W_12.png){:target="_blank"}


<br />

__※ PLURA V5 Web 시스템 관리 메뉴에서 Web Log 수집 설정 방법__
<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/kKLL_sP9w9c' frameborder='0' allowfullscreen></iframe></div>


