---
title: 대상 웹 access 로그
permalink: logcol_web_acc_sys.html
sidebar: faq_siem_M
topnav: topnav
---

시나리오는 다음과 같습니다.

클라이언트의 웹 액세스(access) 로그를 **“PLURA V5 Log Collector 서버”**  이용하여 전송하는 방법

 

** * PLURA V5 Log Collector 서버 이용 장점은 클라이언트(Web Server) 에서 암호화, 압축하지 않고 syslog 로 바로 전송하므로 리소스 사용량 (CPU, Memory 등)을 최소화할 수 있습니다.**

[![image](/docs/images/Additianal/logcol/1.png){: width="800" }](/docs/images/Additianal/logcol/1.png){: target="_blank"}

 

#### 1. 클라이언트: Apache Httpd 웹 접속 로그를 생성

* 환경: CentOS 7 (64비트), Rsyslog 8.24.0-57.el7_9.1

1) **rsyslog.conf 생성 및 remote rsyslog 서버로 전송 수정**

     #vi /etc/rsyslog.d/80-httpd-remote.conf

     #variables required for non-syslog log file forwarding – plura weblog
     #edit on your location

     input(type=”imfile”
     File=”/var/log/plura/weblog.log”
     Tag=”httpd”
     Severity=”info”
     Facility=”local7″)

     ###### Creates a template for each log file in the Logentries UI
     ### logic to apply the relevant templates to the different log files

     if $programname == ‘httpd’ then @PLURA_Log_Collector_Server:514 #UDP
     :programname, isequal, “httpd” stop


 <font color='dodgerblue'> PLURA V5 웹 로깅 경로 /var/log/plura/weblog.log </font>

 <font color='red'> 주의: PLURA V5 웹로그 수집 OFF </font>

<br />
**2) rsyslog restart**

     # service rsyslog restart

<br />
**3) 서버 접속 debug**

     # nc -zu PLURA_Log_Collector_Server 514

     Connection to PLURA_Log_Collector_Server 514 port [udp/syslog] succeeded!

 <br />
## 2. 서버 Log Collector

* 환경: CentOS 7, Rsyslog 8.2010.0

<br />
**1) [PLURA V5 Log Collector 서버 설치](https://qubitsec.github.io/p_agent_lin_srv.html){: target="_blank"}**

<br />
**2) Remote 클라이언트의 syslog 전송 오픈**

     # firewall-cmd –add-port 514/udp

     # firewall-cmd –reload

<br />
**3) 77-plura.conf 수정**

     #vi /etc/rsyslog.d/77-plura.conf

     $template CEETemplate, “%msg:2:$:%\n”

     # Provides UDP syslog reception
     $ModLoad imudp
     $UDPServerRun 514

<br />
**4) 99-plura.conf 수정**

     #vi /etc/rsyslog.d/99-plura.conf

     $template DynaFile, “/var/log/plura/weblog-%FROMHOST-IP%.log”
     *.* -?DynaFile;CEETemplate

<br />
**5) rsyslog restart**

     # service rsyslog restart

<br />
**6) 경로에 파일 수신 여부 확인**

     # ls -al /var/log/plura/

<br />
**7) Log Collector 등록**

[![image](/docs/images/Additianal/logcol/2.png)](/docs/images/Additianal/logcol/2.png){: target="_blank"}


외부 참고 사이트

[https://rsyslog.readthedocs.io/en/latest/configuration/modules/imfile.html](https://rsyslog.readthedocs.io/en/latest/configuration/modules/imfile.html){: target="_blank"}