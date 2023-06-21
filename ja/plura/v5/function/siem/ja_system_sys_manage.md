---
title: システム管理
permalink: ja_system_sys_manage.html
sidebar: M_SIEM_ja
topnav: topnav_ja
---

     PLURA V5 サービスをインストールすると、システム管理ページにシステムの詳細情報が残され、グループの作成およびシステムの状態を変更することができます。

<br />

## 1. システム Summary

- システムSummaryでは、登録されたシステム、動作中のシステム、正常に動作中のエージェント、Windows/LinuxなどのOS別システム数の現状を提供します。

- それぞれのSummary数字をクリックすると、その情報でフィルタされた情報が表示されます。 
<!-- [![image](/docs/images/Manual/siem/system/1.png){: width="800" }](/docs/images/Manual/siem/system/1.png){: target="_blank"}-->

<br />

- PLURA Log Collector (PLC) で表示される情報の意味は以下の通りです。
<!-- [![image](/docs/images/Manual/siem/system/2.png)](/docs/images/Manual/siem/system/2.png){: target="_blank"}-->   
P : Parent(親), C : Child(子)

<br />

- PLURA Log Collector (PLC)(親)の役割
     - 子(システム、アプリケーション、ウェブ、ネットワーク)システムのsyslogを収集
     - 収集したsyslog を圧縮して暗号化し、PLURA V5 クラウドに転送

<br />

PLURA Log Collector (PLC) の詳細については、以下のリンクをご参照ください。

- Install Agents > SIEM > PLC > System : [https://qubitsec.github.io/ja_logcol_system.html](https://qubitsec.github.io/ja_logcol_system.html){:target="_blank"}

<br />

## 2. システム情報

- このシステムをクリックすると、システムIPアドレス、オペレーティングシステムバージョン、アップデートバージョン、エージェントのインストール時間を確認できます。
- アップデート(ビルド)バージョンのマウスオーバー時、該当するHotFix情報を確認することができます。
- アップデート情報がない場合、HotFix情報は表示されません。  
<!-- [![image](/docs/images/Manual/siem/system/3.png){: width="800" }](/docs/images/Manual/siem/system/3.png){: target="_blank"}-->

<br />

## 3. 設定

- そのシステムのウェブログ収集、フルログ保存、リソース収集の設定ができます。
- 変更点を修正するには、そのシステムをクリックし、ON/OFFの状態を変更し、修正ボタンをクリックします。 
<!-- [![image](/docs/images/Manual/siem/system/4.png){: width="800" }](/docs/images/Manual/siem/system/4.png){: target="_blank"}-->

<br />

## 4. ヒストリー

- 複数のフィルタ設定により、収集されたコマンドおよび更新ヒストリーを表示できます。 
<!-- [![image](/docs/images/Manual/siem/system/5.png){: width="800" }](/docs/images/Manual/siem/system/5.png){: target="_blank"}-->

 
<br />

## 5. グループ登録

- グループを追加するには、<グループ登録> をクリックし、グループ名を入力し、追加ボタンを押して追加したいシステムを選択します。
<!-- [![image](/docs/images/Manual/siem/system/6.png){: width="800" }](/docs/images/Manual/siem/system/6.png){: target="_blank"}-->

<br />

- 登録完了ポップアップウィンドウが表示されたら、確認ボタンを押すとグループ登録が完了します。

 
<br />

## 6. システム削除

- 必要に応じてシステムの削除も可能です。 システムリストの左側にあるチェックボックスにチェックすると表示される '削除' ボタンをクリックすると、そのシステムが削除されます。
- PLURA V5サーバーとの通信が正常な時に削除すると、そのシステムにインストールされたエージェントも削除されます。.   
<!-- [![image](/docs/images/Manual/siem/system/7.png)](/docs/images/Manual/siem/system/7.png){: target="_blank"}-->