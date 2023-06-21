---
title: Application
permalink: ja_logcol_application.html
sidebar: Install_A_S_ja
topnav: topnav_ja
---

     PLURA Log Collector (PLC) - Applicationの役割

     1. 他システムのApplication logを取り込み
     2. 取り込み後、Application logを圧縮、暗号化して、PLURA V5へ転送。

<br />

PLURA Log Collector (PLC)サポートOSは下記の通りです。

[https://qubitsec.github.io/ja_support_os.html](https://qubitsec.github.io/ja_support_os.html){:target="_blank"}

<br />

     メーカーがサポートを終了した製品についてPLURA V5でもサポートを終了します。
     PLURA V5でサポートされていないオペレーティングシステムバージョンを使用すると、問題が発生する可能性があります。
     メーカーがサポートを終了したバージョンを使用している場合は、アップグレードについてより積極的な検討が必要です。
     ハッキングや障害など、さまざまな問題に直面し、深刻な問題に発展する可能性があるからです。

<br />

## PLURA Log Collector (PLC) – Application設定。

<br />

### 1. リモート(子)サーバーにアプリケーション転送モジュールインストール


[![image](/docs/images/Ins_G/LogCol_app/ja_app_1.png){: width="800" }](/docs/images/Ins_G/LogCol_app/ja_app_1.png){: target="_blank"}

<br />

### 2. ログ取り込みサーバー(親)にPLCインストール(by root)

`# sudo -s`

`# curl https://repo.plura.io/v5/PLC/install.sh | bash`

<br />

### 3. ログ取り込みサーバー(親)でインバウンドTCP 5514 ホットをオープン

<br />

### 4. ログ取り込みサーバー(親)でライセンス登録及び実行

[![image](/docs/images/Ins_G/LogCol_app/ja_app_3.png){: width="800" }](/docs/images/Ins_G/LogCol_app/ja_app_3.png){: target="_blank"}

<br />

### 5. リモート(子)サーバー登録

- システム  > システム管理 > ログ取り込みサーバー(親)選択 > アプリケーションボタンをクリックします。
[![image](/docs/images/Ins_G/LogCol_app/ja_app_4.png){: width="800" }](/docs/images/Ins_G/LogCol_app/ja_app_4.png){: target="_blank"}

- システム登録ポップアップ > リモート(子)サーバー情報を入力します。
[![image](/docs/images/Ins_G/LogCol_app/ja_app_5.png)](/docs/images/Ins_G/LogCol_app/ja_app_5.png){: target="_blank"}

<br />

- 登録ポップアップで“パス登録”ボタンをクリックします。
[![image](/docs/images/Ins_G/LogCol_app/ja_app_6.png)](/docs/images/Ins_G/LogCol_app/ja_app_6.png){: target="_blank"}

<br />

- タグ及びパスを登録します。
[![image](/docs/images/Ins_G/LogCol_app/ja_app_7.png)](/docs/images/Ins_G/LogCol_app/ja_app_7.png){: target="_blank"}

- タグ登録方法
   - アプリケーションログ取り込みのためのタグを登録出来ます。
   - パス : 管理 > リスト > アプリケーションタグ 
[![image](/docs/images/Ins_G/LogCol_app/ja_app_8.png){: width="800" }](/docs/images/Ins_G/LogCol_app/ja_app_8.png){: target="_blank"}

<br />

- 登録したタグ及び収集しようとするアプリケーションパスを登録します。   
   - 下記の例はApache-errorlogを設定しました。
[![image](/docs/images/Ins_G/LogCol_app/ja_app_9.png)](/docs/images/Ins_G/LogCol_app/ja_app_9.png){: target="_blank"}

<br />

- ログ取り込みサーバー(親)を選択して、アプリケーションログ取り込みが正常に設定されているか確認します。   
   - リモート(子)サーバーを選択すると設定ポップアップが出ます。
[![image](/docs/images/Ins_G/LogCol_app/ja_app_10.png){: width="800" }](/docs/images/Ins_G/LogCol_app/ja_app_10.png){: target="_blank"}

<br />

- アプリケーションログ設定ボタンをOFF → ONにアクティブさせます。 
[![image](/docs/images/Ins_G/LogCol_app/ja_app_11.png)](/docs/images/Ins_G/LogCol_app/ja_app_11.png){: target="_blank"}

<br />

### 6. 収集されたログ確認

- 全ログ > アプリケーションメニューで収集したログが確認出来ます。
[![image](/docs/images/Ins_G/LogCol_app/ja_app_12.png){: width="800" }](/docs/images/Ins_G/LogCol_app/ja_app_12.png){: target="_blank"}