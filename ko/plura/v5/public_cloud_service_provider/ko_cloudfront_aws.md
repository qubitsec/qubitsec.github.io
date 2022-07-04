---
title: WAF의 AWS CloudFront 환경 지원
permalink: ko_cloudfront_aws.html
sidebar: PCSP
topnav: topnav
---


## 1. Amazon CloudFront란?  
[https://docs.aws.amazon.com/ko_kr/AmazonCloudFront/latest/DeveloperGuide/Introduction.html](https://docs.aws.amazon.com/ko_kr/AmazonCloudFront/latest/DeveloperGuide/Introduction.html){:target="_blank"}

<br />

## 2. Amazon CloudFront 환경의 웹서비스 구성 예

[![image](/docs/images/Public_Cloud/cloudfront/01.png){: width="800"  }](/docs/images/Public_Cloud/cloudfront/01.png){: target="_blank"}

위와 같은 환경에서 CloudFront 와 ELB(또는 웹서버) 사이에 PLURA V5 WAF 를 구성할 수 있습니다.

<br />

## 3. CloudFront + PLURA WAF 구성 예

[![image](/docs/images/Public_Cloud/cloudfront/02.png){: width="800"  }](/docs/images/Public_Cloud/cloudfront/02.png){: target="_blank"}