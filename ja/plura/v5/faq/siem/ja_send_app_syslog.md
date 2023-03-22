---
title: Tomcat catalina.outログ
permalink: ja_send_app_syslog.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

シナリオは下記の通りです。

     クライアントのアプリケーションログを“PLURA V5 Log Collectorサーバー”を使用して転送する方法

     アプリケーションログの中、この例ではTomcat8のcatalina.outを使用します。

     PLURA V5 Log Collectorサーバー使用の利点はクライアント(Web Server)に別のログを生成せずにsyslogにすぐ転送するので、リソース使用量
     （CPU、メモリなど）を最小限に抑えることができます。 

<br />

 <!-- [![image](/docs/images/Additianal/send/1.png){: width="800" }](/docs/images/Additianal/send/1.png){: target="_blank"}-->

<br />

## 1. クライアント: Tomcat8のcatalina.out

 환경: CentOS 6 (64ビット), Rsyslog 5.8.10

<br /> 

### 1-1. rsyslog.confダウンロード

`# curl -s https://repo.plura.io/v5/module/rsyslog/v5-stable/00-imfile.conf -o /etc/rsyslog.d/00-imfile.conf`

`# curl -s https://repo.plura.io/v5/module/rsyslog/v5-stable/80-tomcat.conf -o /etc/rsyslog.d/80-tomcat.conf`

<br />

### 1-2. rsyslog.conf remote rsyslogサーバーに転送修正

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

### 1-4. サーバー接続debug

`# nc -zu PLURA_Log_Collector_Server 514`

     Connection to PLURA_Log_Collector_Server 514 port [udp/syslog] succeeded!

<br />

## 2. サーバー

 환경 : CentOS 7, Rsyslog 8.2010.0

<br />

### 2-1. [PLURA V5 Log Collector サーバーインストール](https://qubitsec.github.io/ja_logcol_application.html){: target="_blank"}

<br />

### 2-2. Remote クライアントのsyslog転送オープン

`# firewall-cmd –add-port 514/udp`

`# firewall-cmd –reload`

<br />

### 2-3. パスにファイル受信可否確認

`# ls -al /var/log/plura/`

<br />

内部ブログ

[アプリケーションログ収集 – PLURA’S BLOG](https://qubitsec.github.io/ja_rsys_log.html){: target="_blank"}

<br />

外部参考サイト

[https://www.rsyslog.com/doc/v5-stable/configuration/modules/imfile.html](https://www.rsyslog.com/doc/v5-stable/configuration/modules/imfile.html){: target="_blank"}

[https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html](https://www.rsyslog.com/doc/v8-stable/configuration/modules/imfile.html){: target="_blank"}

[http://linuxsysconfig.com/how-to-configure-remote-logging-on-rhel6-centos6/](http://linuxsysconfig.com/how-to-configure-remote-logging-on-rhel6-centos6/){: target="_blank"}

[https://www.teimouri.net/centralized-logs-rsyslog/](https://www.teimouri.net/centralized-logs-rsyslog/){: target="_blank"}

 