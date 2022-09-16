---
title: PLURA WAF 환경
permalink: ko_waf_no_cloudfront_aws.html
sidebar: PCSP
topnav: topnav
---


## 1. Amazon CloudFront란?  
[https://docs.aws.amazon.com/ko_kr/AmazonCloudFront/latest/DeveloperGuide/Introduction.html](https://docs.aws.amazon.com/ko_kr/AmazonCloudFront/latest/DeveloperGuide/Introduction.html){:target="_blank"}

<br />

## 2. Amazon CloudFront 환경의 웹서비스 구성 예

(CloudFront 없는 구성)

설정 값에 따라 자동으로 WAF 확장 시스템 (Autoscaling)

[![image](/docs/images/Public_Cloud/cloudfront/04.png){: width="800"  }](/docs/images/Public_Cloud/cloudfront/04.png){: target="_blank"}

위와 같은 환경에서 CloudFront 와 ELB(또는 웹서버) 사이에 PLURA V5 WAF 를 구성할 수 있습니다.

