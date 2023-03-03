---
title: Tomcat access ロギングオン
permalink: ja_apache_tom_acc.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

     TomcatのaccessログをPLURA V5ロギング(logging)連動設定する方法です。

<br />

Tomcat server.xmlファイルにロギング関連設定を修正します。

     # Change for PLURA log format

     <Valve className=”org.apache.catalina.valves.AccessLogValve” directory=”/var/log/plura”
     rotatable=”false”
     renameOnRotate=”false”
     prefix=”weblog” suffix=”.log”
     pattern=”{“Remote-addr”: “%a”, “X-forwarded-for”: “%{X-Forwarded-For}i”, “Request-date”: “%{dd/MM/yyyy:HH:mm:ss.SSS}t +0900”, “Method”: “%m”, “Request”: “%r”, “Host”: “%A”, “Uri”: “%U”, “Cookie”: “%{Cookie}i”, “Referer”: “%{Referer}i”, “User-Agent”: “%{User-Agent}i”, “Status”: “%s”, “Resp-Content-Length”: “%b”}” />

<br />

 pattern内”は`&quot;`修正する必要があります。.

<!-- [![image](/docs/images/Additianal/apache/1.png){: width="800" }](/docs/images/Additianal/apache/1.png){: target="_blank"}-->

▶ Git source, [https://github.com/QubitSecurity/ModPlura/tree/main/tomcat](https://github.com/QubitSecurity/ModPlura/tree/main/tomcat){: target="_blank"}

<br />

Tomcat logging.propertiesファイルにロギング関連設定を修正します。

     2localhost.org.apache.juli.AsyncFileHandler.directory = /var/log/plura
     2localhost.org.apache.juli.AsyncFileHandler.prefix = weblog.
     2localhost.org.apache.juli.FileHandler.suffix = log

<br />

Tomcatリブート

`# systemctl restart tomcat8`

<br />

Tomcatをウェブシステムとして認識させるコマンド

`# echo “ModPlura-tomcat” > /etc/modplura`

`# echo “0.0.1” >> /etc/modplura`

`# touch /etc/.modplura`

<br />

Tomcat accessログファイルに権限付与

`# touch /var/log/plura/weblog.log`

`# chmod -R 766 /var/log/plura/weblog.log`

`# chcon -t syslog_log_t /var/log/plura/weblog.log`

<br />

内部ブログ

[Apache Tomcat catalina.out ロギング](https://qubitsec.github.io/ja_send_app_syslog.html){: target="_blank"}

 <br />

参考サイト

[https://tomcat.apache.org/tomcat-9.0-doc/config/valve.html](https://tomcat.apache.org/tomcat-9.0-doc/config/valve.html){: target="_blank"}

[https://m.blog.naver.com/solinsystem/221796167356](https://m.blog.naver.com/solinsystem/221796167356){: target="_blank"}

[https://gyrfalcon.tistory.com/entry/Apache-Tomcat-access-log-%EC%84%A4%EC%A0%95](https://gyrfalcon.tistory.com/entry/Apache-Tomcat-access-log-%EC%84%A4%EC%A0%95){: target="_blank"}

[https://gyrfalcon.tistory.com/entry/Apache-Tomcat-access-log-%EC%84%A4%EC%A0%95](https://gyrfalcon.tistory.com/entry/Apache-Tomcat-access-log-%EC%84%A4%EC%A0%95){: target="_blank"}

[https://stackoverflow.com/questions/39896222/how-to-include-time-format-with-millisecond-precision-in-apache-access-log](https://stackoverflow.com/questions/39896222/how-to-include-time-format-with-millisecond-precision-in-apache-access-log){: target="_blank"}