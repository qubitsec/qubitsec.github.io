---
title: 시스템 관리
permalink: system_manage_for.html
sidebar: M_for
topnav: topnav
---

     PLURA V5 서비스를 설치하면 시스템 관리 페이지에 시스템의 상세 정보가 남게 되며, 그룹 생성 및 시스템의 상태를 변경할 수 있습니다.


## 1.시스템 Summary

- 시스템 Summary에서는 등록된 시스템, 동작중인 시스템, 정상적으로 동작 중인 에이전트, 윈도우/리눅스 등 OS별 시스템 수 현황을 제공합니다.

- 각각의 Summary 숫자를 클릭하는 경우, 해당 정보로 필터된 정보가 노출됩니다.

[![image](/docs/images/Manual/forensic/system/1.png){: width="800" }](/docs/images/Manual/forensic/system/1.png){: target="_blank"}

- Syslog Collector에서 노출되는 정보의 의미는 아래와 같습니다.

[![image](/docs/images/Manual/forensic/system/2.png)](/docs/images/Manual/forensic/system/2.png){: target="_blank"}

      P : Parent(부모), C : Child(자식)

<br />
- PLURA V5 Syslog Collector(부모) 의 역할

      자식(네트워크 장비 또는 다른 시스템)시스템의 syslog 를 취합
      취합한 syslog 를 압축하고 암호화하여 PLURA V5 클라우드로 전송

<br />
- PLURA V5 Syslog Collector Server 지원 OS는 다음과 같습니다.
      CentOS/RHEL 6, 7, 8
      AWS AMI 2018
      AWS Linux AMI 2
      Ubuntu 16, 18, 20

<br />
     제조사가 지원을 종료한 제품에 대하여 PLURA V5에서도 지원을 종료합니다.

     PLURA V5에서 지원하지 않는 운영체제 버전을 사용한다면 문제가 발생할 수 있습니다.

     제조사가 지원 종료한 버전을 사용 중이라면 업그레이드에 대하여 보다 적극적인 검토가 필요합니다. 
     해킹과 장애 등 다양한 문제에 직면하고 심각한 문제로 발전할 수 있기 때문입니다.

PLURA V5 Syslog Collector에 대한 자세한 내용은 아래의 링크를 참고해주세요.
- Install Guide > SIEM > PLURA V5 Syslog Collector Srv  : http://blog.plura.io/?p=7186

<br />
## 2.최신순/ 오래된순 선택

- 최신순 또는 오래된순으로 선택해서 볼 수 있습니다.

[![image](/docs/images/Manual/forensic/system/3.png)](/docs/images/Manual/forensic/system/3.png){: target="_blank"}

<br />
## 3.라인 수 선택

- 한 페이지에 표시될 라인 수를 선택할 수 있습니다.

[![image](/docs/images/Manual/forensic/system/4.png){: width="800" }](/docs/images/Manual/forensic/system/4.png){: target="_blank"}

<br />
## 4.그룹 선택

- 그룹을 선택할 수 있습니다.

[![image](/docs/images/Manual/forensic/system/5.png){: width="800" }](/docs/images/Manual/forensic/system/5.png){: target="_blank"}

<br />
## 5.운영체제 선택

- 원하는 운영체제를 선택할 수 있습니다.

[![image](/docs/images/Manual/forensic/system/6.png){: width="800" }](/docs/images/Manual/forensic/system/6.png){: target="_blank"}
 
<br />
## 6.시스템 IP주소 선택

- 원하는 시스템 IP주소를 선택할 수 있습니다.

[![image](/docs/images/Manual/forensic/system/7.png){: width="800" }](/docs/images/Manual/forensic/system/7.png){: target="_blank"}

<br />
## 7.취합로그 선택

- 모든 취합된 로그를 보거나 시스템, 시스템/웹으로 분류하여 볼 수 있습니다.

[![image](/docs/images/Manual/forensic/system/8.png){: width="800" }](/docs/images/Manual/forensic/system/8.png){: target="_blank"}

<br />
## 8.등록방법 선택

- 라이센스로 등록하거나, 직접 등록한 방법을 선택해서 볼 수 있습니다.

[![image](/docs/images/Manual/forensic/system/9.png){: width="800" }](/docs/images/Manual/forensic/system/9.png){: target="_blank"}
 
<br />
## 9.전체로그(수집) 선택

- 전체로그의 수집 상태별로 선택해서 볼 수 있습니다.

[![image](/docs/images/Manual/forensic/system/10.png){: width="800" }](/docs/images/Manual/forensic/system/10.png){: target="_blank"}
 
<br />
## 10.그룹등록

- 그룹을 추가하려면 ‘그룹등록’을 클릭한 후 그룹명을 입력한 후 추가버튼을 눌러 추가하고싶은 시스템을 선택합니다.

[![image](/docs/images/Manual/forensic/system/11.png){: width="800" }](/docs/images/Manual/forensic/system/11.png){: target="_blank"}

- 등록완료 팝업창이 나타나면 확인 버튼을 누르면 그룹 등록이 완료됩니다.

 
<br />
## 11.시스템 삭제

- 시스템 리스트 왼쪽의 체크박스에 체크하면 나타나는 ‘삭제’ 버튼을 클릭하면 해당 시스템이 삭제됩니다.

[![image](/docs/images/Manual/forensic/system/12.png){: width="800" }](/docs/images/Manual/forensic/system/12.png){: target="_blank"}

 