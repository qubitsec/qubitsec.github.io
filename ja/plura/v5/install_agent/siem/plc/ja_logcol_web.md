---
title: Web
permalink: ja_logcol_web.html
sidebar: Install_A_S_ja
topnav: topnav_ja
---

     PLURA Log Collector (PLC) - Webの役割

     – 他のシステムのWeblogを取り込み
     – 取り込みしたログを圧縮、暗号化してPLURA V5クラウドに転送

<br />

PLURA Log Collector (PLC)サポートOSは次の通りです.

[https://qubitsec.github.io/ja_support_os.html](https://qubitsec.github.io/ja_support_os.html){:target="_blank"}

<br />

     メーカーがサポートを終了した製品についてPLURA V5でもサポートを終了します。
     PLURA V5でサポートされていないオペレーティングシステムバージョンを使用すると、問題が発生する可能性があります。
     メーカーがサポートを終了したバージョンを使用している場合は、アップグレードについてより積極的な検討が必要です。
     ハッキングや障害など、さまざまな問題に直面し、深刻な問題に発展する可能性があるからです。

<br />

## PLURA Log Collector (PLC) – Web設定

<br />

### 1.　ログ取り込みサーバー(親)にPLCインストール(by root)

`# sudo -s`

`# curl https://repo.plura.io/v5/PLC/install.sh | bash`

<br />

### 2. ライセンス登録及び実行

[![image](/docs/images/Ins_G/LogCol_web/ja_2.png){: width="800" }](/docs/images/Ins_G/LogCol_web/ja_2.png){:target="_blank"}

<br />

### 3. ウェブログモジュールインストール

[![image](/docs/images/Ins_G/LogCol_web/ja_3.png){: width="800" }](/docs/images/Ins_G/LogCol_web/ja_3.png){:target="_blank"}

<br />

### 4. 環境設定

`# vi /etc/datos/conf/httplogger.conf`   

[![image](/docs/images/Ins_G/LogCol_web/ja_4.png){: width="800" }](/docs/images/Ins_G/LogCol_web/ja_4.png){:target="_blank"}

<br />

### 5. ログ取り込みサーバー(親)にポットミラーリング構成

<br />

### 6. リモート(子)サーバー登録

<br />

#### 6-1. リモート(子)登録パス

- システム  > システム管理 > ログ取り込みサーバー(親)選択 > ウェブボタンをクリックします。
[![image](/docs/images/Ins_G/LogCol_web/ja_5.png){: width="800" }](/docs/images/Ins_G/LogCol_web/ja_5.png){:target="_blank"}

#### 6-2. 情報入力

- システム登録ポップアップ > リモート(子)サーバー情報を入力します。
[![image](/docs/images/Ins_G/LogCol_web/ja_6.png)](/docs/images/Ins_G/LogCol_web/ja_6.png){:target="_blank"}

#### 6-3.登録完了

- システム > システム管理ページでリモート(子)サーバーが登録されました。 
<!-- [![image](/docs/images/Ins_G/LogCol_web/7.png){: width="800" }](/docs/images/Ins_G/LogCol_web/7.png){:target="_blank"} -->

<br />

### 7. 収集されたログ確認

- 全ログ > ウェブメニューで収集されたログが確認出来ます。
<!-- [![image](/docs/images/Ins_G/LogCol_web/8.png){: width="800" }](/docs/images/Ins_G/LogCol_web/8.png){:target="_blank"} -->