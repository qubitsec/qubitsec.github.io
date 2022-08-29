---
title: squid 로깅 켜기
permalink: ko_proxy_sys_squid.html
sidebar: faq_siem_M
topnav: topnav
---

Forward 프록시로 squid 사용할 때 PLURA V5 로깅(logging) 연동 설정하는 방법입니다.

httpd 와 유사한 로깅 방법은 다음과 같습니다.

     logformat httpd %>a %[ui %[un [%tl] “%rm %ru HTTP/%rv” %>Hs %<st “%{Referer}>h” “%{User-Agent}>h” %Ss:%Sh
     access_log /var/log/squid/access.log httpd

<br />

json 으로 PLURA V5 로깅 형태로 저장하는 방법은 다음과 같습니다.

`# vi /etc/squid/squid.conf`

     forwarded_for on
     acl has-xff req_header X-Forwarded-For ^(([0-9]+\.[0-9]+\.[0-9]+\.[0-9]+)|(\[([0-9a-f]+)?:([0-9a-f:]+)?:([0-9a-f]+|0-9\.]+)?\]))

     # add logging for PLURA
     logformat combinedjson {“Remote-addr”: “%>a”, “X-forwarded-for”: “%{X-Forwarded-For}>h”, “Request-date”: “%tl”, “Method”: “%rm”, “Request”: “%rm %rp HTTP/%rv”, “Host”: “%>rd”, “Uri”: “%ru”, “Resp-Content-Type”: “%mt”, “Refere”: “%{Referer}>h”, “User-Agent”: “%{User-Agent}>h”, “Status”: “%>Hs”, “Resp-Content-Length”: “%<st”, “ProxyStatus”: “%Ss:%Sh”}

     #access_log /var/log/squid/access.log combinedjson
     access_log stdio:/var/log/plura/weblog.log combinedjson !has-xff
     access_log stdio:/var/log/plura/weblog.log combinedjson has-xff

 
<br />

▶ Git source, [https://github.com/QubitSecurity/ModPlura/tree/main/squid](https://github.com/QubitSecurity/ModPlura/tree/main/squid){: target="_blank"}

squid 를 웹 시스템으로 인식하게 하는 명령어

`# echo “ModPlura-squid” > /etc/modplura`

`# echo “0.0.1” >> /etc/modplura`

`# touch /etc/.modplura`

<br />

squid access 로그 파일에 권한 부여하기

`# touch /var/log/plura/weblog.log`

`# chmod -R 766 /var/log/plura/weblog.log`

`# chcon -t squid_log_t /var/log/plura/weblog.log`

 <br />

**PLURA V5 > 시스템 > 시스템 관리**에서 리스트의 시스템을 확장하면 다음과 같이 확인됩니다.

 [![image](/docs/images/Additianal/proxy/1.png)](/docs/images/Additianal/proxy/1.png){: target="_blank"}

<br />

참고 사이트

[http://www.squid-cache.org/Doc/config/logformat/](http://www.squid-cache.org/Doc/config/logformat/){: target="_blank"}

[https://bit.ly/36DjfZ3](https://bit.ly/36DjfZ3){: target="_blank"}

[https://bit.ly/3hzt6Fw](https://bit.ly/3hzt6Fw){: target="_blank"}

[https://gist.github.com/kosho/82546a86140ad67c866e8197d730c53c](https://gist.github.com/kosho/82546a86140ad67c866e8197d730c53c){: target="_blank"}

 <br />

참고사이트 XFF

[https://gist.github.com/alvarow/fa409edc70aeb4cf89bbc83c1c78f392](https://gist.github.com/alvarow/fa409edc70aeb4cf89bbc83c1c78f392){: target="_blank"}