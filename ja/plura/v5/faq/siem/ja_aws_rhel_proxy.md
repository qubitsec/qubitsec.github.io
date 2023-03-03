---
title: AWS RHEL環境
permalink: ja_aws_rhel_proxy.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

RHELシステムでPLURA V5クラウドサービス接続のためProxyシステムを一緒に使用する場合、
下記の通りProxy設定をする必要があります。     

`# vi /etc/profile.d/plura.sh`

      http_proxy=http://(Proxy IPアドレス):(Proxyポート)
      https_proxy=$http_proxy
      no_proxy=”127.0.0.1, amazonlinux.ap-northeast-2.amazonaws.com”
      export http_proxy https_proxy no_proxy

<br />

**例**

 <!-- [![image](/docs/images/Additianal/aws/1.png)](/docs/images/Additianal/aws/1.png){: target="_blank"}-->

 <br />

**プロキシを経由した接続テスト**

`# curl -v https://repo.plura.io`