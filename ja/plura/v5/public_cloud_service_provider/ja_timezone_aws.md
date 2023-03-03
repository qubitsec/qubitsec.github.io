---
title: AWSでタイムゾーン設定
permalink: ja_timezone_aws.html
sidebar: PCSP_ja
topnav: topnav_ja
---

すべてのロギング システムで最も重要なのは、時間同期です。

AWS では Local Time の既定値として "GMT" が設定されます。

<br />

## 1. ローカルタイムをAsia/seoulに時間設定変更する方法

`# ln -sf /usr/share/zoneinfo/Asia/Seoul /etc/localtime`

<br />

## 2. rsyslog再起動

rsyslogを再起動しないと、収集ログの時間が変更適用されません。

`# service rsyslog restart`

<br />

**シナリオ1_現在 Local time 確認**

`# date`
<!-- [![image](/docs/images/Public_Cloud/timezone/01.png){: width="800" }](/docs/images/Public_Cloud/timezone/01.png){: target="_blank"}-->  

LocaltimeがMon Jul 602:16:00 UTC 2020に設定されています。

<br />

**シナリオ2_現在のLocal timeをAsia/seoulに設定変更**

`# ln -sf /usr/share/zoneinfo/Asia/Seoul /etc/localtime`
<!-- [![image](/docs/images/Public_Cloud/timezone/02.png){: width="800" }](/docs/images/Public_Cloud/timezone/02.png){: target="_blank"}-->

LocaltimeがMon Jul 6 11:16:42 KST 2020に変更されました。

<br />

**シナリオ3_rsyslog再起動**

`# service rsyslog restart`

<br />

***シナリオの結果、Localtimeが変更されました。**

(既存) Mon Jul 602:16:00 UTC 2020

→ （変更）Mon Jul 6 11:16:42 KST 2020

<br />

## 3.PLURAページの時間設定方法

PLURA > 管理 > システム > 時間

Windowsサーバの場合、UTC基準で時間が設定され、使用する国のローカルタイムを設定する必要があります。