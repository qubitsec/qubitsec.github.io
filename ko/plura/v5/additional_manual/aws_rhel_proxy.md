---
title: AWS RHEL 8 에서 Proxy 환경으로 PLURA V5 사용 시 설정
permalink: aws_rhel_proxy.html
sidebar: Add_M
topnav: topnav
---

PLURA V5 클라우드 서비스 접속을 위하여 Proxy 시스템을 두어 운영하는 경우,
다음과 같이 Proxy 설정을 해야 합니다.

– vi /etc/profile.d/plura.sh

      http_proxy=http://(Proxy IP주소):(Proxy 포트)
      https_proxy=$http_proxy
      no_proxy=”127.0.0.1, amazonlinux.ap-northeast-2.amazonaws.com”
      export http_proxy https_proxy no_proxy

– 예시

 [![image](/docs/images/Additianal/aws/1.png)](/docs/images/Additianal/aws/1.png){: target="_blank"}

 

– 프록시를 경유한 접속 테스트

      # curl -v https://repo.plura.io