---
title: 톰캣 catalina.out 로그
permalink: send_app_syslog.html
sidebar: faq_siem_M
topnav: topnav
---

**시나리오는 다음과 같습니다.**

     클라이언트의 응용프로그램 로그를 “PLURA V5 Log Collector 서버” 이용하여 전송하는 방법

     응용프로그램 로그 중에 이번 예제에서는 Tomcat8 의 catalina.out 을 사용합니다.

     PLURA V5 Log Collector 서버 이용 장점은 클라이언트(Web Server) 에 별도 로그를 생성하지 않고 syslog 로 바로 전송하므로 리소스 사용량 (CPU, Memory 등)을 최소화할 수 있습니다.

 [![image](/docs/images/Additianal/send/1.png){: width="800" }](/docs/images/Additianal/send/1.png){: target="_blank"}

<br />

## 1. 클라이언트: Tomcat8 의 catalina.out

 환경: CentOS 6 (64비트), Rsyslog 5.8.10

<br /> 

### 1-1. rsyslog.conf 다운로드

`# curl -s https://repo.plura.io/v5/module/rsyslog/v5-stable/00-imfile.conf -o /etc/rsyslog.d/00-imfile.conf`

`# curl -s https://repo.plura.io/v5/module/rsyslog/v5-stable/80-tomcat.conf -o /etc/rsyslog.d/80-tomcat.conf`

<br />

### 1-2. rsyslog.conf remote rsyslog 서버로 전송 수정

`# vi /etc/rsyslog.d/80-tomcat.conf`

     #variables required for non-syslog log file forwarding – application log file
     #edit on your location

     $InputFileName /var/log/tomcat8/catalina.out
     $InputFileTag tomcat8:
     $InputFileStateFile stat-catalina.out

     $InputFileSeverity info
     $InputFileFacility local7
     $InputRunFileMonitor

     # Send to remote rsyslog server using UDP
     if $programname == ‘tomcat8’ then @PLURA_Log_Collector_Server:514 #UDP
     :programname, isequal, “tomcat8” ~

<br />

### 1-3. rsyslog restart

`# service rsyslog restart`

<br />

### 1-4. 서버 접속 debug

`# nc -zu PLURA_Log_Collector_Server 514`

     Connection to PLURA_Log_Collector_Server 514 port [udp/syslog] succeeded!

<br />

## 2. 서버

 환경: CentOS 7, Rsyslog 8.2010.0

<br />

### 2-1. [PLURA V5 Log Collector 서버 설치](https://qubitsec.github.io/p_agent_lin_srv.html){: target="_blank"}

<br />

### 2-2. Remote 클라이언트의 syslog 전송 오픈

`# firewall-cmd –add-port 514/udp`

`# firewall-cmd –reload`

<br />

### 2-3. 경로에 파일 수신 여부 확인

`# ls -al /var/log/plura/`

<br />

내부 블로그

[응용프로그램 로그 수집 – PLURA’S BLOG](https://qubitsec.github.io/rsys_log.html){: target="_blank"}

 

외부 참고 사이트

[https://www.rsyslog.com/doc/v5-stable/configuration/modules/imfile.html](https://www.rsyslog.com/doc/v5-stable/configuration/modules/imfile.html){: target="_blank"}

[https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html](https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html){: target="_blank"}

[http://linuxsysconfig.com/how-to-configure-remote-logging-on-rhel6-centos6/](http://linuxsysconfig.com/how-to-configure-remote-logging-on-rhel6-centos6/){: target="_blank"}

[https://www.teimouri.net/centralized-logs-rsyslog/](https://www.teimouri.net/centralized-logs-rsyslog/){: target="_blank"}

 