---
title: PLURA WAF 環境(With CloudFront)
permalink: ja_waf_cloudfront_aws.html
sidebar: PCSP_ja
topnav: topnav_ja
---


## 1. Amazon CloudFrontとは?  
[https://docs.aws.amazon.com/ja_kr/AmazonCloudFront/latest/DeveloperGuide/Introduction.html](https://docs.aws.amazon.com/ja_kr/AmazonCloudFront/latest/DeveloperGuide/Introduction.html){:target="_blank"}

<br />

## 2. CloudFront + PLURA-WAF 構成例

(CloudFrontがある構成)

設定値に応じて自動的にWAFシステム拡張(Autoscaling)

<!-- [![image](/docs/images/Public_Cloud/cloudfront/03.png){: width="800"  }](/docs/images/Public_Cloud/cloudfront/03.png){: target="_blank"}-->

上記のような環境でALB(またはウェブサーバ)間にPLURA-WAFを構成することができます。