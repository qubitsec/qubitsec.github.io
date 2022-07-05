---
title: AWS 인스턴스에 53 DNS 할당
permalink: ko_route_53_dns.html
sidebar: PCSP
topnav: topnav
---

Amazon EC2인스턴스 IP 어드레싱  
[https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/using-instance-addressing.html](https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/using-instance-addressing.html){:target="_blank"}

AWS 인스턴스를 생성할 때 자동으로 할당되는 DNS 보다 우선되도록 Route 53 DNS를 할당할 수 있습니다.  
아래와 같은 순서로 진행합니다.

<br />

## 1. DHCP 옵션 세트 생성

사용하려는 DNS를 할당하여 새 DHCP 옵션 세트 생성  

[https://docs.aws.amazon.com/ko_kr/vpc/latest/userguide/VPC_DHCP_Options.html](https://docs.aws.amazon.com/ko_kr/vpc/latest/userguide/VPC_DHCP_Options.html){:target="_blank"}

<br />

## 2. DHCP 옵션 세트 연결  

새 VPC를 생성하거나 기존의 VPC에 위에서 생성한 DHCP 옵션 세트를 연결  

[https://docs.aws.amazon.com/ko_kr/vpc/latest/userguide/vpc-dns.html](https://docs.aws.amazon.com/ko_kr/vpc/latest/userguide/vpc-dns.html){:target="_blank"}

<br />
 
## 3. 인스턴스 연결  

위에서 설정한 VPC를 인스턴스에 연결  

[https://aws.amazon.com/ko/premiumsupport/knowledge-center/connect-vpc/](https://aws.amazon.com/ko/premiumsupport/knowledge-center/connect-vpc/){:target="_blank"}