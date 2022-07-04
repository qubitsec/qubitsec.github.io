---
title: 톰캣 access 로깅 켜기
permalink: ko_apache_tom_acc.html
sidebar: faq_siem_M
topnav: topnav
---

     Tomcat의 access 로그를 PLURA V5 로깅(logging) 연동 설정하는 방법입니다.

<br />

Tomcat server.xml 파일에 로깅 관련 설정을 수정합니다.

     # Change for PLURA log format

     <Valve className=”org.apache.catalina.valves.AccessLogValve” directory=”/var/log/plura”
     rotatable=”false”
     renameOnRotate=”false”
     prefix=”weblog” suffix=”.log”
     pattern=”{“Remote-addr”: “%a”, “X-forwarded-for”: “%{X-Forwarded-For}i”, “Request-date”: “%{dd/MM/yyyy:HH:mm:ss.SSS}t +0900”, “Method”: “%m”, “Request”: “%r”, “Host”: “%A”, “Uri”: “%U”, “Cookie”: “%{Cookie}i”, “Referer”: “%{Referer}i”, “User-Agent”: “%{User-Agent}i”, “Status”: “%s”, “Resp-Content-Length”: “%b”}” />

<br />

 pattern 내의 ” 은 `&quot;` 수정해야 함.

[![image](/docs/images/Additianal/apache/1.png){: width="800" }](/docs/images/Additianal/apache/1.png){: target="_blank"}

▶ Git source, [https://github.com/QubitSecurity/ModPlura/tree/main/tomcat](https://github.com/QubitSecurity/ModPlura/tree/main/tomcat){: target="_blank"}

<br />

Tomcat logging.properties 파일에 로깅 관련 설정을 수정합니다.

     2localhost.org.apache.juli.AsyncFileHandler.directory = /var/log/plura
     2localhost.org.apache.juli.AsyncFileHandler.prefix = weblog.
     2localhost.org.apache.juli.FileHandler.suffix = log

<br />

Tomcat 재 시작

`# systemctl restart tomcat8`

<br />

Tomcat 을 웹 시스템으로 인식하게 하는 명령어

`# echo “ModPlura-tomcat” > /etc/modplura`

`# echo “0.0.1” >> /etc/modplura`

`# touch /etc/.modplura`

<br />

Tomcat access 로그 파일에 권한 부여하기

`# touch /var/log/plura/weblog.log`

`# chmod -R 766 /var/log/plura/weblog.log`

`# chcon -t syslog_log_t /var/log/plura/weblog.log`

<br />

내부 블로그

Apache Tomcat catalina.out 로깅하기

[응용프로그램 로그 syslog 전송하기 – PLURA’S BLOG](https://qubitsec.github.io/ko_send_app_syslog.html){: target="_blank"}

 <br />

참고 사이트

[https://tomcat.apache.org/tomcat-9.0-doc/config/valve.html](https://tomcat.apache.org/tomcat-9.0-doc/config/valve.html){: target="_blank"}

 

[https://m.blog.naver.com/solinsystem/221796167356](https://m.blog.naver.com/solinsystem/221796167356){: target="_blank"}

[https://gyrfalcon.tistory.com/entry/Apache-Tomcat-access-log-%EC%84%A4%EC%A0%95](https://gyrfalcon.tistory.com/entry/Apache-Tomcat-access-log-%EC%84%A4%EC%A0%95){: target="_blank"}

[https://gyrfalcon.tistory.com/entry/Apache-Tomcat-access-log-%EC%84%A4%EC%A0%95](https://gyrfalcon.tistory.com/entry/Apache-Tomcat-access-log-%EC%84%A4%EC%A0%95){: target="_blank"}

[https://stackoverflow.com/questions/39896222/how-to-include-time-format-with-millisecond-precision-in-apache-access-log](https://stackoverflow.com/questions/39896222/how-to-include-time-format-with-millisecond-precision-in-apache-access-log){: target="_blank"}