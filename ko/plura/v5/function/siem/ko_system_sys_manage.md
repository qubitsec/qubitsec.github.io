---
title: 시스템 관리
permalink: ko_system_sys_manage.html
sidebar: M_SIEM
topnav: topnav
---

     PLURA V5 서비스를 설치하면 시스템 관리 페이지에 시스템의 상세 정보가 남게 되며, 그룹 생성 및 시스템의 상태를 변경할 수 있습니다.

<br />

## 1. 시스템 Summary

- 시스템 Summary에서는 등록된 시스템, 동작중인 시스템, 정상적으로 동작 중인 에이전트, 윈도우/리눅스 등 OS별 시스템 수 현황을 제공합니다.

- 각각의 Summary 숫자를 클릭하는 경우, 해당 정보로 필터된 정보가 노출됩니다.   
[![image](/docs/images/Manual/siem/system/1.png){: width="800" }](/docs/images/Manual/siem/system/1.png){: target="_blank"}

<br />

- PLURA Log Collector (PLC) 에서 노출되는 정보의 의미는 아래와 같습니다.   
[![image](/docs/images/Manual/siem/system/2.png)](/docs/images/Manual/siem/system/2.png){: target="_blank"}   
P : Parent(부모), C : Child(자식)

<br />

- PLURA Log Collector (PLC) (부모) 의 역할
     - 자식(시스템, 응용프로그램, 웹, 네트워크)시스템의 syslog 를 취합
     - 취합한 syslog 를 압축하고 암호화하여 PLURA V5 클라우드로 전송

<br />

PLURA Log Collector (PLC) 에 대한 자세한 내용은 아래의 링크를 참고해주세요.

- Install Agents > SIEM > PLC > System : [https://qubitsec.github.io/ko_logcol_system.html](https://qubitsec.github.io/ko_logcol_system.html){:target="_blank"}

<br />

## 2. 시스템 정보

- 해당 시스템을 클릭하면 시스템IP주소, 운영체제 버전, 업데이트 버전, 에이전트 설치시간을 확인할 수 있습니다.
- 업데이트(빌드) 버전 마우스 오버 시, 해당 HotFix 정보를 확인할 수 있습니다.
- 업데이트 정보가 없는 경우, HotFix 정보는 노출되지 않습니다.   
[![image](/docs/images/Manual/siem/system/08.png){: width="800" }](/docs/images/Manual/siem/system/08.png){: target="_blank"}

<br />

## 3. 설정

- 해당 시스템의 웹로그 수집, 전체로그 저장, 리소스 수집 설정을 할 수 있습니다.
- 변경사항을 수정하려면 해당 시스템을 클릭한 후 ON/OFF 상태를 변경하고 수정 버튼을 클릭합니다.   
[![image](/docs/images/Manual/siem/system/4.png){: width="800" }](/docs/images/Manual/siem/system/4.png){: target="_blank"}

<br />

## 4. 히스토리

- 여러 필터 설정에 따라 수집된 명령어 및 업데이트 히스토리를 볼 수 있습니다.   
[![image](/docs/images/Manual/siem/system/5.png){: width="800" }](/docs/images/Manual/siem/system/5.png){: target="_blank"}

 
<br />

## 5. 그룹등록

- 그룹을 추가하려면 ‘그룹등록’을 클릭한 후 그룹명을 입력한 후 추가 버튼을 눌러 추가하고 싶은 시스템을 선택합니다.   
[![image](/docs/images/Manual/siem/system/6.png){: width="800" }](/docs/images/Manual/siem/system/6.png){: target="_blank"}

<br />

- 등록완료 팝업창이 나타나면 확인 버튼을 누르면 그룹 등록이 완료됩니다.

 
<br />

## 6. 시스템 삭제

- 필요 시 시스템 삭제도 가능합니다. 시스템 리스트 왼쪽의 체크박스에 체크하면 나타나는 ‘삭제’버튼을 클릭하면 해당 시스템이 삭제됩니다.
- PLURA V5 서버와 통신이 정상일 때 삭제하면 해당 시스템에 설치된 에이전트도 삭제됩니다.   
[![image](/docs/images/Manual/siem/system/7.png)](/docs/images/Manual/siem/system/7.png){: target="_blank"}

<br />

## 7. 협의된 네트워크 로그 수집 등록

- 협의된 네트워크 로그 수집 등록은 Public-Syslog 서비스로서, 에이전트를 설치할 수 없는 환경의 Syslog를 수집할 수 있는 서비스입니다.
[![image](/docs/images/Manual/siem/system/09.png){: width="800" }](/docs/images/Manual/siem/system/09.png){: target="_blank"}

- IP주소 입력의 경우, 외부로 통신하는 IP주소를 입력해주세요.
- 정렬코드 : 업로드되는 로그의 programname이 없는 경우, 정렬코드 여부 설정으로 임의의 programname을 생성하여 msg정렬을 할 수 있습니다. 기본값은 OFF 이며 필요 시 시스템 환경에 따라 큐비트시큐리티와 협의하여 수정이 필요합니다.
- 모든 정보를 등록한 후, 큐비트시큐리티로 연락주시면 후속 지원해드리겠습니다.
