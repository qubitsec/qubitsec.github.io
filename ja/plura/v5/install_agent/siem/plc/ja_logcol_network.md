---
title: Network
permalink: ja_logcol_network.html
sidebar: Install_A_S_ja
topnav: topnav_ja
---

     PLURA Log Collector (PLC) - Networkの役割

     – 他のネットワークデバイスなどのシステムログをSyslog形で取り込み
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

## PLURA Log Collector (PLC) – Network設定

<br />

### 1. リモート(子)デバイスにSyslog転送設定。
**※ 下位システム設定**

- Syslog転送設定(by root)

  `# vi /etc/rsyslog.conf`
     
        <例>
        *.info @ログ取り込みシステムIPアドレス

<br />

- Syslogリブート

  `# service rsyslog restart`

<br />

### 2. ログ取り込みサーバー(親)にPLCインストール(by root)

`# sudo -s`
`# curl https://repo.plura.io/v5/PLC/install.sh | bash`

<br />

### 3. ライセンス登録及び実行

`# /etc/plura/plura.sh registerライセンスキー`

<br />

### 4. リモート(子)サーバー登録

- システム  > システム管理 > ログ取り込みサーバー(親)選択 > ネットワークボタンをクリックします。
[![image](/docs/images/Ins_G/LogCol_Net/ja_3.png){: width="800" }](/docs/images/Ins_G/LogCol_Net/ja_3.png){:target="_blank"}

- システム登録ポップアップ > リモート(子)デバイス情報を入力します。
[![image](/docs/images/Ins_G/LogCol_Net/ja_4.png)](/docs/images/Ins_G/LogCol_Net/ja_4.png){:target="_blank"}

- システム > システム管理ページでリモート(子)デバイスが登録されました。
[![image](/docs/images/Ins_G/LogCol_Net/ja_5.png){: width="800" }](/docs/images/Ins_G/LogCol_Net/ja_5.png){:target="_blank"}

<br />

### 5. 収集されたログ確認

- 全ログ > システムメニューで収集されたログが確認出来ます。
<!-- [![image](/docs/images/Ins_G/LogCol_Net/6.png){: width="800" }](/docs/images/Ins_G/LogCol_Net/6.png){:target="_blank"} -->
