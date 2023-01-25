---
title: squidロギングオン
permalink: ja_proxy_sys_squid.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

Forwardプロキシでsquidを使用する時、PLURA V5ロギング(logging)連動設定方法です。

httpdと同様のロギング方法は下記の通りです。

     logformat httpd %>a %[ui %[un [%tl] “%rm %ru HTTP/%rv” %>Hs %<st “%{Referer}>h” “%{User-Agent}>h” %Ss:%Sh
     access_log /var/log/squid/access.log httpd

<br />

jsonでPLURA V5ロギング形式で保存する方法は下記の通りです。

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

squidをウェブシステムとして認識させるコマンド

`# echo “ModPlura-squid” > /etc/modplura`

`# echo “0.0.1” >> /etc/modplura`

`# touch /etc/.modplura`

<br />

squid accessログファイルに権限付与

`# touch /var/log/plura/weblog.log`

`# chmod -R 766 /var/log/plura/weblog.log`

`# chcon -t squid_log_t /var/log/plura/weblog.log`

 <br />

**PLURA V5 > システム > システム管理**でリストのシステムを拡張すると、下記のように確認されます。

 [![image](/docs/images/Additianal/proxy/1.png)](/docs/images/Additianal/proxy/1.png){: target="_blank"}

<br />

参考サイト

[http://www.squid-cache.org/Doc/config/logformat/](http://www.squid-cache.org/Doc/config/logformat/){: target="_blank"}

[https://bit.ly/36DjfZ3](https://bit.ly/36DjfZ3){: target="_blank"}

[https://bit.ly/3hzt6Fw](https://bit.ly/3hzt6Fw){: target="_blank"}

[https://gist.github.com/kosho/82546a86140ad67c866e8197d730c53c](https://gist.github.com/kosho/82546a86140ad67c866e8197d730c53c){: target="_blank"}

 <br />

参考サイト XFF

[https://gist.github.com/alvarow/fa409edc70aeb4cf89bbc83c1c78f392](https://gist.github.com/alvarow/fa409edc70aeb4cf89bbc83c1c78f392){: target="_blank"}