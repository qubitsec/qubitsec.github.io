---
title: EC2 Auto Scaling 환경 지원
permalink: ko_amazon_ec2_scaling.html
sidebar: PCSP
topnav: topnav
---

## 1. Amazon EC2 Auto Scaling 이란?  
[https://docs.aws.amazon.com/ko_kr/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html](https://docs.aws.amazon.com/ko_kr/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html){:target="_blank"}

<br />

## 2. Amazon EC2 Auto Scaling 환경의 구성 예

[![image](/docs/images/Public_Cloud/ec2_autoscaling/01.png)](/docs/images/Public_Cloud/ec2_autoscaling/01.png){: target="_blank"}  
그림 출처 : https://docs.aws.amazon.com

위와 같은 환경에서 각각의 인스턴스에 PLURA 에이전트를 설치하여 사용할 수 있습니다.  
인스턴스가 그룹에서 분리되거나 Standby 상태가 되어도 시스템이 종료되는 것이 아니라 Auto Scaling 그룹과 연결된 탄력적 로드 밸런서에서 해당 인스턴스가 제거되어 트래픽이 로드 밸런서에서 이들 인스턴스로 라우트되지 않을 뿐이므로 PLURA 에이전트는 계속해서 로그를 취합합니다.

<br />

## 3. PLURA 에이전트 설정

PLURA 에이전트에서 다음과 같이 Auto Scaling 에서 활용할 기능을 설정할 수 있습니다.

     [root@localhost]# vi /etc/plura/conf/plura.conf

     1. 시스템 기동 시 에이전트 로그인 지연 설정  
     login_delay_sec = 0 (초)

     2. AWS 환경에서 Auto Scaling 사용 시 인스턴스 고유의 식별자를 PLURA V5 시스템으로 전송하는 설정(값이 1일때 전송)  
     login_with_machine_id = 0

     3. 여러개의 네트워크 인터페이스를 사용할 때 PLURA V5 웹에 표시되는 IP주소 설정  
     interface = eth1 (시스템 > 시스템 관리 리스트에 보이는 대표 IP주소를 지정)  
     interface_mon = eth1 (시스템 > 리소스 모니터링 > 네트워크 트래픽을 수집 할 인터페이스 설정)
      
     4. 시스템 기동 시 hostname 변경에 따른 로그인 지연 설정  
     login_hostname_check=0 (default = 0)  
     0 > 지정된 지연시간까지 무조건 기다림  
     1 > hostname 변경이 1회 감지되면 지연 중단  
     2 > hostname 변경이 2번 감지되면 지연 중단