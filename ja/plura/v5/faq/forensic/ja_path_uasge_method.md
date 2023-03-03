---
title: オペレーティングシステムログアップロード収集パス及び使用方法
permalink: ja_path_uasge_method.html
sidebar: faq_forensic_M_ja
topnav: topnav_ja
---

     PLURA V5 Forensicは収集されたシステム(OS)のログをアップロードして分析出来るサービスです。

     アップロードされたログは事前に定義されたマイターアタックなど数千の異常行為を検出できるポリシーによって自動に分析されるので
     従来のログ分析業務方式と比べて99.9999%以上の業務負荷を減らせます。


## 1. オペレーティングシステム(OS)種類別ログ収集パス

<br />

### 1-1. ウィンドウズ

`C:\Windows\System32\winevt\Logs`

<!-- [![image](/docs/images/Additianal/path/1.png){: width="800" }](/docs/images/Additianal/path/1.png){: target="_blank"}-->

<br />

### 1-2. linux – Redhat/CentOS系

`/var/log/messages`

<br />

### 1-3. linux – Ubuntu系

`/var/log/syslog`

<br />

## 2. PLURA V5 Forensicエージェントでログのアップロードする方法

<br />

### 2-1. PLURA V5 Forensic エージェントログイン

<!-- [![image](/docs/images/Additianal/path/2.png){: width="800" }](/docs/images/Additianal/path/2.png){: target="_blank"}-->

<br />

### 2-2. ログアップロードを進行するオペレーティングシステム及びログ年度選択

<!-- [![image](/docs/images/Additianal/path/3.png){: width="800" }](/docs/images/Additianal/path/3.png){: target="_blank"}-->

<br />

### 2-3. 情報及びパス入力

システム/ホスト名/ニックネームの入力後、“Select”ボタンをクリックしてログがあるパスを選択してください。

<!-- [![image](/docs/images/Additianal/path/4.png){: width="800" }](/docs/images/Additianal/path/4.png){: target="_blank"}-->

<br />

### 2-4. “Start”ボタンをクリックしてログアップロード進行

<!-- [![image](/docs/images/Additianal/path/5.png){: width="800" }](/docs/images/Additianal/path/5.png){: target="_blank"}-->

<br />

### 2-5. アップロード中止

ログアップロードの進行中には“START”ボタンが“STOP”ボタンになり, アップロードを中止できます。

<!-- [![image](/docs/images/Additianal/path/6.png){: width="800" }](/docs/images/Additianal/path/6.png){: target="_blank"}-->

<br />

### 2-6. ログアップロード方法

PLURA V5で正常にアップロードされたログを確認してください。

<!-- [![image](/docs/images/Additianal/path/7.png){: width="800" }](/docs/images/Additianal/path/7.png){: target="_blank"}-->
 
<br />

     メーカーがサポートを終了した製品についてPLURAV5でもサポートを終了します。
     PLURAV5でサポートされていないオペレーティングシステムバージョンを使用すると、問題が発生する可能性があります。
     メーカーがサポートを終了したバージョンを使用している場合は、アップグレードについてより積極的な検討が必要です。
     ハッキングや障害など、さまざまな問題に直面し、深刻な問題に発展する可能性があるからです。

<br />

**内部ブログ**

PLURA V5 Forensicエージェントインストール方法

[https://qubitsec.github.io/ko_forensic.html](https://qubitsec.github.io/ko_forensic.html){: target="_blank"}