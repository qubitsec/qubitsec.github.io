---
title: Web
permalink: logcol_web.html
sidebar: Install_G_S
product: Install_G_S
---

     PLURA V5 Log Collector-Web의 역할

     – 다른 시스템의 Weblog 를 취합
     – 취합한 Weblog 를 압축하고 암호화하여 PLURA V5 클라우드로 전송

PLURA V5 Syslog Collector Server 지원 OS는 다음과 같습니다.

     CentOS 7, Stream 8
     RHEL 7, 8
     AWS Linux 2 AMI
     Ubuntu 18.04, 20.04, 22.04

     제조사가 지원을 종료한 제품에 대하여 PLURA V5에서도 지원을 종료합니다.

     PLURA V5에서 지원하지 않는 운영체제 버전을 사용한다면 문제가 발생할 수 있습니다.

     제조사가 지원 종료한 버전을 사용 중이라면 업그레이드에 대하여 보다 적극적인 검토가 필요합니다. 
     해킹과 장애 등 다양한 문제에 직면하고 심각한 문제로 발전할 수 있기 때문입니다.

### PLURA V5 Log Collector – Web 설정하기

__1. 로그 취합서버(부모)에 로그콜렉터를 설치합니다.(by root)__

     sudo -s
     curl https://repo.plura.io/v5/logcollector/install.sh | bash

![image](/docs/images/Ins_G/LogCol_web/1.png){: width="700" height="120"}

**2. 라이센스 등록 및 실행을 합니다.**

     /etc/plura/plura.sh register 라이센스키

![image](/docs/images/Ins_G/LogCol_web/2.png){: width="700" height="120"}

**3. 웹로그 모듈을 설치합니다.**

     /etc/plura/plura.sh install_datos

![image](/docs/images/Ins_G/LogCol_web/3.png){: width="700" height="120"}

**4. 환경 설정을 합니다.**

     vi /etc/datos/conf/httplogger.conf

     <예>
     interface = eth0
     logfile = /var/log/plura/weblog.log
     host = 10.100.10.10
     port = 80

![image](/docs/images/Ins_G/LogCol_web/4.png){: width="700" height="150"}

**5. 로그 취합 서버(부모)에 포트미러링을 구성합니다.**

**6. 원격지(자식) 서버를 등록합니다.**
  ① 시스템  > 시스템 관리 > 로그 취합서버(부모) 선택 > 웹 버튼을 클릭합니다.

![image](/docs/images/Ins_G/LogCol_web/5.png){: width="650" height="400"}

② 시스템 등록 팝업 > 원격지(자식) 서버 정보를 입력합니다.

![image](/docs/images/Ins_G/LogCol_web/6.png){: width="650" height="400"}

③ 시스템 > 시스템 관리 페이지에서 원격지(자식) 서버가 등록되었습니다. 

![image](/docs/images/Ins_G/LogCol_web/7.png){: width="700" height="300"}

**7. 전체로그 > 웹 메뉴에서 수집된 로그를 확인할 수 있습니다.**

![image](/docs/images/Ins_G/LogCol_web/8.png){: width="700" height="350"}