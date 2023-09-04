---
title: Sysmon (Windows Sysinternals)
permalink: ja_sysmon.html
sidebar: Install_A_E_ja
product: Install_A_E_ja
---

## Sysmonインストール<!-- 映像 -->

<!-- <style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/G6crbYg2Mzw' frameborder='0' allowfullscreen></iframe></div> -->

<br />

     Sysmonはデフォルトウィンドウイベントログでは限界があるプロセス生成、ネットワーク制限などをイベント化出来ます。
     事故対応の観点から生成されたプロセスリストとネットワーク接続ログは事故を再構成することに非常に役立ちます
     Sysmonは別のモニタリングツールがなくてもドライバーのインストールだけで上記のログをイベント化させます。
     サーバー管理者はサービス中のサーバーで使用されているドライバーとSysmonドライバーの競合可否を確認する必要があります。

<br />

## 1. Sysmonインストール

Sysmonをインストールするにはまず __PLURA V5 Agent__ をインストールする必要があります。   
インストール後、下記の内容を参照してSysmonをインストールします。

[Agentインストールページ](https://qubitsec.github.io/ja_p_agent_win_srv.html){:target="_blank"}

<br />

### 1-1. オプション

最新バージョンダウンロードリンク : [ Sysmon ](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon){:target="_blank"}

圧縮ファイルを解凍して、Sysmonフォルダーㅏで **[Shift + 右クリック]** をして‘ここでコマンドウィンドウを開く’でcmdウィンドウを起動します.

[![image](/docs/images/Ins_G/Sysmon/ja_sysmon_1.png)](/docs/images/Ins_G/Sysmon/ja_sysmon_1.png){:target="_blank"}

**” Sysmon.exe –i [options] ”コマンドでSysmonをインストール出来ます。**
**” Sysmon.exe -h ”コマンドで[options]のリストが確認出来ます。**

**[options]**

[![image](/docs/images/Ins_G/Sysmon/ja_sysmon_2.png)](/docs/images/Ins_G/Sysmon/ja_sysmon_2.png){:target="_blank"}

インストールする時 **-accepteula** オプションを使用するとソフトウェアユーザー同意者 **EULA(End User License Agreement)** を自動にOK状態からインストール出来ます。

Sysmonのオプション関連説明は[ダウンロードページ](https://docs.microsoft.com/ko-kr/sysinternals/downloads/sysmon){:target="_blank"}にも上手く説明されています。

<br />

### 1-2. 実行

#### 1-2-1. ファイルダウンロード

- sysmon-plura.xmlファイルを下記のパスからダウンロードします。

     [https://github.com/QubitSecurity/sysmon/blob/master/sysmon-plura.xml](https://github.com/QubitSecurity/sysmon/blob/master/sysmon-plura.xml){:target="_blank"}

     PLURA V5エージェントをインストールするとPLURAフォルダーで確認出来ます。

     - **パス : C:\Program Files\PLURA**

<br />

#### 1-2-2. コマンド入力

- ダウンロードしたSysmonファイルパスでCMDウィンドウ(管理者権限)を実行し、下記のコマンドを入力します。

`# sysmon.exe -accepteula -i “C:\Program Files\PLURA\sysmon-plura.xml”`

<br />

### 1-3. 確認

AgentでSysmonインストール確認

[![image](/docs/images/Ins_G/Sysmon/ja_sysmon_3.png)](/docs/images/Ins_G/Sysmon/ja_sysmon_3.png){:target="_blank"}

<br />

## 2. Sysmonイベント確認

SysmonがインストールされるとウィンドウサービスログパスにSysmonログが追加されます。

%SystemRoot%\System32\Winevt\Logs\Microsoft-Windows-Sysmon%4Operational.evtx

[![image](/docs/images/Ins_G/Sysmon/ja_sysmon_4.png)](/docs/images/Ins_G/Sysmon/ja_sysmon_4.png){:target="_blank"}

<br />

## 3. Sysmon活用

イベントビューアで下記の通りアプリケーション及びサービスログ->Microsoft->Windows->Sysmon-> Operationalがクリック出来ます。

[![image](/docs/images/Ins_G/Sysmon/ja_sysmon_5.png)](/docs/images/Ins_G/Sysmon/ja_sysmon_5.png){:target="_blank"}

[![image](/docs/images/Ins_G/Sysmon/ja_sysmon_6.png){: width="800" }](/docs/images/Ins_G/Sysmon/ja_sysmon_6.png){:target="_blank"}

  - Sysmon Event IDの定義は次のURLで確認出来ます。

    [https://docs.microsoft.com/ko-kr/sysinternals/downloads/sysmon](https://docs.microsoft.com/ko-kr/sysinternals/downloads/sysmon){:target="_blank"}
 
<br />

## 4. Sysmonログ確認

- SysmonログをPLURA V5ウェブページで確認出来ます。
- フィルタ検出 > システム > チャンネル"Sysmon"選択
- 全ログ > システム > チャンネル"Sysmon"選択

      メーカーがサポートを終了した製品についてPLURA V5でもサポートを終了します。
      PLURA V5でサポートされていないオペレーティングシステムバージョンを使用すると、問題が発生する可能性があります。
      メーカーがサポートを終了したバージョンを使用している場合は、アップグレードについてより積極的な検討が必要です。
      ハッキングや障害など、さまざまな問題に直面し、深刻な問題に発展する可能性があるからです。