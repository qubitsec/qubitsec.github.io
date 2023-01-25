---
title: 対象ウェブaccessログ
permalink: ja_logcol_web_acc_sys.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

シナリオは下記の通りです。

     クライアントウェブアクセス(access)ログを“PLURA V5 Log Collectorサーバ”使用して転送する方法

     PLURA V5 Log Collectorサーバ利点はクライアント(Web Server)で暗号化, 圧縮せずにsyslogにすぐ転送するためリソース使用量
     （CPU、メモリなど）を最小限に抑えることができます。 

<br />

[![image](/docs/images/Additianal/logcol/1.png){: width="800" }](/docs/images/Additianal/logcol/1.png){: target="_blank"}

<br />

## 1. クライアント: Apache Httpdウェブ接続ログ生成

 環境: CentOS 7 (64ビット), Rsyslog 8.24.0-57.el7_9.1

<br />

**1-1. rsyslog.conf生成及びremote rsyslogサーバで転送修正**

`# vi /etc/rsyslog.d/80-httpd-remote.conf`

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


 <font color='dodgerblue'> PLURA V5ウェブロギングパス/var/log/plura/weblog.log </font>
 
 <br />
 
 <font color='red'> 注意: PLURA V5ウェブログ収集OFF </font>

<br />

**1-2. rsyslog restart**

`# service rsyslog restart`

<br />

**1-3. サーバ接続debug**

`# nc -zu PLURA_Log_Collector_Server 514`

     Connection to PLURA_Log_Collector_Server 514 port [udp/syslog] succeeded!

 <br />

## 2. サーバLog Collector

 環境 : CentOS 7, Rsyslog 8.2010.0

<br />

**2-1. [PLURA V5 Log Collectorサーバインストール](https://qubitsec.github.io/ja_logcol_application.html){: target="_blank"}**

<br />

**2-2. Remote クライアントのsyslog転送オープン**

`# firewall-cmd –add-port 514/udp`

`# firewall-cmd –reload`

<br />

**2-3. 77-plura.conf修正**

`# vi /etc/rsyslog.d/77-plura.conf`

     $template CEETemplate, “%msg:2:$:%\n”

     # Provides UDP syslog reception
     $ModLoad imudp
     $UDPServerRun 514

<br />

**2-4. 99-plura.conf修正**

`# vi /etc/rsyslog.d/99-plura.conf`

     $template DynaFile, “/var/log/plura/weblog-%FROMHOST-IP%.log”
     *.* -?DynaFile;CEETemplate

<br />

**2-5. rsyslog restart**

`# service rsyslog restart`

<br />

**2-6. パスにファイル受信可否確認**

`# ls -al /var/log/plura/`

<br />

**2-7. Log Collector登録**

パス : システム > システム管理 > ログ取り込みサーバ(親)選択 > 収集環境選択

[![image](/docs/images/Additianal/logcol/2.png)](/docs/images/Additianal/logcol/2.png){: target="_blank"}

<br />

外部参考サイト

[https://rsyslog.readthedocs.io/en/latest/configuration/modules/imfile.html](https://rsyslog.readthedocs.io/en/latest/configuration/modules/imfile.html){: target="_blank"}