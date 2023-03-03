---
title: System
permalink: ja_logcol_system.html
sidebar: Install_A_S_ja
topnav: topnav_ja
---


     PLURA Log Collector (PLC) - Systemの役割

     1. 他のシステムのsyslogを取り込み
     2. 取り込みしたログを圧縮、暗号化してPLURA V5クラウドに転送

<br />

PLURA Log Collector (PLC)サポートOSは次の通りです.

[https://qubitsec.github.io/ja_support_os.html](https://qubitsec.github.io/ja_support_os.html){:target="_blank"}

<br />

     メーカーがサポートを終了した製品についてPLURAV5でもサポートを終了します。
     PLURAV5でサポートされていないオペレーティングシステムバージョンを使用すると、問題が発生する可能性があります。
     メーカーがサポートを終了したバージョンを使用している場合は、アップグレードについてより積極的な検討が必要です。
     ハッキングや障害など、さまざまな問題に直面し、深刻な問題に発展する可能性があるからです。

<br />

## PLURA Log Collector (PLC) – System設定

<br />

### 1. 遠距離(子)サーバにSyslog転送設定

<br />

__※ 下位システム設定__

Syslog転送設定(by root)

`# vi /etc/rsyslog.conf`

     <例>

     *.info @ログ取り込みシステムIPアドレス

<br />

Syslogリブート

`# service rsyslog restart`

<br />

### 2. ログ取り込みサーバ(親)にPLCインストール(by root)


`# sudo -s`

`# curl https://repo.plura.io/v5/PLC/install.sh | bash`

<br />

### 3. ライセンス登録及び実行

`# /etc/plura/plura.sh registerライセンスキー`

<br />

### 4. 遠距離(子)サーバ登録

- システム  > システム管理 > ログ取り込みサーバ(親)選択 > システムボタンをクリックします。
<!-- [![image](/docs/images/Ins_G/logCol_system/sys_3.png){: width="800" }](/docs/images/Ins_G/logCol_system/sys_3.png){:target="_blank"} -->

<br />

- システム登録ポップアップ > 遠距離(子)サーバ情報を入力します。
<!-- [![image](/docs/images/Ins_G/logCol_system/sys_4.png)](/docs/images/Ins_G/logCol_system/sys_4.png){:target="_blank"} -->

<br />

- システム > システム管理ページで遠距離(子)サーバが登録されました。
<!-- [![image](/docs/images/Ins_G/logCol_system/sys_5.png){: width="800" }](/docs/images/Ins_G/logCol_system/sys_5.png){:target="_blank"} -->

<br />

### 5. 収集されたログ確認

- 全ログ > システムメニューで収集されたログが確認出来ます。
<!-- [![image](/docs/images/Ins_G/logCol_system/sys_6.png){: width="800" }](/docs/images/Ins_G/logCol_system/sys_6.png){:target="_blank"} -->