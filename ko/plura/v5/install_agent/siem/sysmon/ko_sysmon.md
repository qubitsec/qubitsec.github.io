---
title: Sysmon (Windows Sysinternals)
permalink: ko_sysmon.html
sidebar: Install_A_S
product: Install_A_S
---

## Sysmon 설치 영상

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/G6crbYg2Mzw' frameborder='0' allowfullscreen></iframe></div>

<br />

     Sysmon 은 기본 윈도우 이벤트 로그로는 한계가 있는 프로세스 생성, 네트워크 연결 등을 이벤트화할 수 있습니다. 
     사고 대응 관점에서 생성된 프로세스 목록과 네트워크 연결 로그는 사고를 재구성하는데 굉장히 도움이 됩니다. 
     Sysmon 은 별도의 모니터링 도구없이 간단히 드라이버 설치만으로 이런 로그를 이벤트화 시켜줍니다.
     서버 관리자는 운영중인 서버에서 사용되는 드라이버와 Sysmon 드라이버의 충돌 여부를 확인해야 합니다.

<br />

## 1. Sysmon 설치

Sysmon 을 설치하려면 먼저 __PLURA V5 Agent__ 를 설치해야합니다.   
PLURA V5 Agent 설치 완료 후 아래의 내용을 참고하여 Sysmon 을 설치합니다.

<br />

### 1-1. 옵션

최신버전 다운로드 링크 : [ Sysmon ](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon){:target="_blank"}

압축을 푼 후 Sysmon 폴더에서 **[Shift + 우클릭]** 을 하여 ‘여기서 명령 창 열기’ 로 cmd 창을 엽니다.

[![image](/docs/images/Ins_G/Sysmon/sysmon_1.png)](/docs/images/Ins_G/Sysmon/sysmon_1.png){:target="_blank"}

**” Sysmon.exe –i [options] ” 명령어를 통해 Sysmon을 설치할 수 있습니다.**
**” Sysmon.exe -h ” 명령어를 통해 [options] 의 목록을 볼 수 있습니다.**

**[options]**

[![image](/docs/images/Ins_G/Sysmon/sysmon_2.png)](/docs/images/Ins_G/Sysmon/sysmon_2.png){:target="_blank"}

설치할 때 **-accepteula** 옵션을 사용하면 소프트에어 사용자 동의인 **EULA(End User License Agreement)** 를 자동 수락된 상태에서 설치가 가능합니다.

Sysmon의 옵션 관련 설명은 [다운로드 페이지](https://docs.microsoft.com/ko-kr/sysinternals/downloads/sysmon){:target="_blank"} 에도 잘 설명되어 있습니다.

<br />

### 1-2. 실행

#### 1-2-1. sysmon-plura.xml 파일을 아래의 경로에서 다운로드합니다.
     [https://github.com/QubitSecurity/sysmon/blob/master/sysmon-plura.xml](https://github.com/QubitSecurity/sysmon/blob/master/sysmon-plura.xml){:target="_blank"}

     PLURA V5 에이전트를 설치하면 PLURA 폴더에서 확인할 수 있습니다.
     경로 : C:\Program Files (x86)\PLURA

<br />

#### 1-2-2. 다운로드 한 Sysmon 파일의 경로에서 CMD창(관리자권한)을 실행 후 아래의 명령어를 입력합니다.

`# sysmon.exe -accepteula -i “C:\Program Files (x86)\PLURA\sysmon-plura.xml”`

<br />

### 1-3. 확인

Agent 에서 SYSMON 설치 확인

[![image](/docs/images/Ins_G/Sysmon/sysmon_3.png)](/docs/images/Ins_G/Sysmon/sysmon_3.png){:target="_blank"}

<br />

## 2. Sysmon 이벤트확인

Sysmon 이 설치되면 윈도우 서비스 로그 경로에 Sysmon 로그가 추가됩니다.

%SystemRoot%\System32\Winevt\Logs\Microsoft-Windows-Sysmon%4Operational.evtx

[![image](/docs/images/Ins_G/Sysmon/sysmon_4.png)](/docs/images/Ins_G/Sysmon/sysmon_4.png){:target="_blank"}

<br />

## 3. Sysmon 활용

이벤트뷰어에서 아래와 같이 응용 프로그램 및 서비스 로그->Microsoft->Windows->Sysmon-> Operational 을 클릭할 수 있습니다.

[![image](/docs/images/Ins_G/Sysmon/sysmon_5.png)](/docs/images/Ins_G/Sysmon/sysmon_5.png){:target="_blank"}

[![image](/docs/images/Ins_G/Sysmon/sysmon_6.png){: width="800" }](/docs/images/Ins_G/Sysmon/sysmon_6.png){:target="_blank"}

  - Sysmon Event ID 의 의미는 다음 URL에서 확인할 수 있습니다.

    [https://docs.microsoft.com/ko-kr/sysinternals/downloads/sysmon](https://docs.microsoft.com/ko-kr/sysinternals/downloads/sysmon){:target="_blank"}
 
<br />

## 4. Sysmon 로그를 PLURA V5 웹 페이지에서 확인할 수 있습니다.

- 필터탐지 > 시스템
- 전체로그 > 시스템

      제조사가 지원을 종료한 제품에 대하여 PLURA V5에서도 지원을 종료합니다.
      PLURA V5에서 지원하지 않는 운영체제 버전을 사용한다면 문제가 발생할 수 있습니다.
      제조사가 지원 종료한 버전을 사용 중이라면 업그레이드에 대하여 보다 적극적인 검토가 필요합니다.
      해킹과 장애 등 다양한 문제에 직면하고 심각한 문제로 발전할 수 있기 때문입니다.