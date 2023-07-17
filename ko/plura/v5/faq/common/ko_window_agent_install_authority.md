---
title: 윈도우 에이전트 설치 권한
permalink: ko_window_agent_install_authority.html
sidebar: faq_common_M
topnav: topnav
---

<br />

## Administrator 그룹에 속한 사용자 계정(관리자 계정)

     Administrator 그룹에 속한 사용자 계정(관리자 계정) 으로 PLURA V5 설치 이후 
     로그 오프 또는 시스템 재시작시 시작프로그램에 등록된 Tray 프로그램이 UAC 영향으로 
     실행되지 않을 수 있습니다.
     반면 윈도우 서비스에 등록된 PLURAService.exe 는 System 권한으로 실행되기 때문에 
     영향을 받지 않고 정상 작동하게 됩니다.

<br />

## Administrator 계정

     Administrator 계정은 UAC (User Account Control, 사용자 계정 컨트롤) 의 영향을 받지 않지만 다른 모든 사용자 (Administrators 그룹에 속한 사용자 포함) 는 영향을 받습니다. 
     따라서 PLURA V5 프로그램 설치는 Administrator 계정으로 설치 해야 시스템의 재시작 
     또는 로그오프 이후 재접속시에도 시작메뉴에 등록된 PLURATray.exe 가 정상 작동하게 됩니다. 
     System 권한으로 작동되는 PLURAService.exe 는 영향이 없습니다.