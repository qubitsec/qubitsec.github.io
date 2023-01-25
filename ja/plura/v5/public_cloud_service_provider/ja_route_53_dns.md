---
title: AWS インスタンスに53DNS割り当て
permalink: ja_route_53_dns.html
sidebar: PCSP_ja
topnav: topnav_ja
---

Amazon EC2インスタンスIPアドレッシング 
[https://docs.aws.amazon.com/ja_kr/AWSEC2/latest/UserGuide/using-instance-addressing.html](https://docs.aws.amazon.com/ja_kr/AWSEC2/latest/UserGuide/using-instance-addressing.html){:target="_blank"}

AWSインスタンスを生成する際に自動的に割り当てられるDNSより優先されるようにRoute 53 DNSを割り当てることができます。
以下の手順で進めます。

<br />

## 1. DHCPオプションセットの作成

使用したいDNSを割り当て、新しいDHCPオプションセットを作成

[https://docs.aws.amazon.com/ja_kr/vpc/latest/userguide/VPC_DHCP_Options.html](https://docs.aws.amazon.com/ja_kr/vpc/latest/userguide/VPC_DHCP_Options.html){:target="_blank"}

<br />

## 2. DHCP オプション セット 接続

新しいVPCを生成するか、既存のVPCに上記で生成したDHCPオプションセットを接続

[https://docs.aws.amazon.com/ja_kr/vpc/latest/userguide/vpc-dns.html](https://docs.aws.amazon.com/ja_kr/vpc/latest/userguide/vpc-dns.html){:target="_blank"}

<br />
 
## 3. インスタンス接続

上記で設定したVPCをインスタンスに接続 

[https://aws.amazon.com/ko/premiumsupport/knowledge-center/connect-vpc/](https://aws.amazon.com/ko/premiumsupport/knowledge-center/connect-vpc/){:target="_blank"}