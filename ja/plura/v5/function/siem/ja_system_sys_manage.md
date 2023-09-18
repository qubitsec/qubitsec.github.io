---
title: システム管理
permalink: ja_system_sys_manage.html
sidebar: M_C_ja
topnav: topnav_ja
---

     PLURA V5 サービスをインストールすると、システム管理ページにホストの詳細情報が残され、グループ作成およびホストの状態を変更できます。

<br />

## 1. Summary 

- Summaryでは登録されたホスト、動作中のホスト、正常に動作しているエージェント、Windows/LinuxなどOS別ホスト数の現況を提供します。

- それぞれのSummary数字をクリックすると、その情報でフィルタされた情報が表示されます。   
 [![image](/docs/images/Manual/siem/system/ja/1.PNG){: width="800" }](/docs/images/Manual/siem/system/ja/1.PNG){: target="_blank"} 

<br />

- PLURA Log Collector (PLC) で表示される情報の意味は以下の通りです。

 [![image](/docs/images/Manual/siem/system/ja/2.PNG){: width="200" }](/docs/images/Manual/siem/system/ja/2.PNG){: target="_blank"}    
P : Parent(親), C : Child(子)

<br />

- PLURA Log Collector (PLC) (親)の役割
     - 子(ホスト、アプリケーション、ウェブ、ネットワーク)システムのsyslogを収集
     - 収集したsyslogを圧縮して暗号化し、PLURA V5 クラウドに転送

<br />

PLURA Log Collector (PLC) の詳細については、以下のリンクをご参照ください。

 - Install Agents > SIEM > PLC > System : [https://qubitsec.github.io/ko_logcol_system.html](https://qubitsec.github.io/ko_logcol_system.html){:target="_blank"} 

<br />

## 2. ホスト情報

- 該当するホストをクリックすると、ホストIPアドレス、オペレーティングシステムバージョン、更新バージョン、エージェントのインストール時間を確認できます。
- アップデート(ビルド)バージョンのマウスオーバー時、該当するHotFix情報を確認できます。
- アップデート情報がない場合、HotFix情報は表示されません。
 [![image](/docs/images/Manual/siem/system/ja/3.PNG){: width="800" }](/docs/images/Manual/siem/system/ja/3.PNG){: target="_blank"} 

<br />

## 3. 設定

- 該当するホストのウェブログ収集、全体ログ保存、リソース収集設定ができます。
- 変更点を修正するには、そのホストをクリックし、ON/OFFの状態を変更して修正ボタンをクリックします。
 [![image](/docs/images/Manual/siem/system/ja/4.PNG){: width="800" }](/docs/images/Manual/siem/system/ja/4.PNG){: target="_blank"} 

<br />

- アプリケーションの元のログ設定は、以下に表示されている設定アイコンをクリックして行うことができます。
 [![image](/docs/images/Manual/siem/system/ja/5.PNG)](/docs/images/Manual/siem/system/ja/5.PNG){: target="_blank"} 

- タグとパスを入力したら、登録ボタンをクリックします。
 [![image](/docs/images/Manual/siem/system/ja/6.PNG)](/docs/images/Manual/siem/system/ja/6.PNG){: target="_blank"} 

- 詳しい説明はPLURAブログで確認できます。
[アプリケーションログ分析](http://blog.plura.io/?p=17820){: target="_blank"}

<br />

- EDRエージェントの場合、以下の画像のように分析設定（検知/ブロック/全体ログ収集）を変更することができます。
 [![image](/docs/images/Manual/siem/system/ja/7.PNG){: width="800" }](/docs/images/Manual/siem/system/ja/7.PNG){: target="_blank"} 

<br />

- 「Hタイプ」検索オプションは検知方式によって「検知」または「ブロック」で検索できます。
 [![image](/docs/images/Manual/siem/system/ja/8.PNG)](/docs/images/Manual/siem/system/ja/8.PNG){: target="_blank"} 

<br />

## 4. セキュリティ

- ホストの終了またはネットワーク隔離設定を行うことができます。
※ 重複使用不可（ホスト終了orネットワーク隔離のいずれか1つのみ使用）
  - ネットワーク隔離の場合、PLURAエージェントを除くすべてのネットワークをブロックします。
  - ログアップロード、検知、ブロックなどPLURAエージェントは正常に動作します。
 [![image](/docs/images/Manual/siem/system/ja/9.PNG){: width="800" }](/docs/images/Manual/siem/system/ja/9.PNG){: target="_blank"} 

- セキュリティタブは、以下のパスからメニュー表示設定を行うことができます。
  - 管理 > 使用 > ホスト > ユーザー設定

<br />

## 5. ヒストリー

- 複数のフィルタ設定により、収集されたコマンドおよび更新ヒストリーを表示できます。
 [![image](/docs/images/Manual/siem/system/ja/10.PNG){: width="800" }](/docs/images/Manual/siem/system/ja/10.PNG){: target="_blank"} 

<br />

## 6. チャンネル別ログ数

- 選択したシステムのチャネルごとのログ数を確認できます。
※ Windows、Linuxの場合にのみボタンが提供されます。
 [![image](/docs/images/Manual/siem/system/ja/11.PNG){: width="800" }](/docs/images/Manual/siem/system/ja/11.PNG){: target="_blank"} 

<br />

- チャネルごとのログ数アイコンを選択すると、ポップアップが表示されます。
 [![image](/docs/images/Manual/siem/system/ja/12.PNG){: width="800" }](/docs/images/Manual/siem/system/ja/12.PNG){: target="_blank"} 

<br />

## 7. グループ登録

- グループを追加するには、[グループ登録] をクリックし、グループ名を入力し、追加ボタンを押して追加したいホストを選択します。
 [![image](/docs/images/Manual/siem/system/ja/13.PNG){: width="800" }](/docs/images/Manual/siem/system/ja/13.PNG){: target="_blank"} 

<br />

- 登録完了ポップアップウィンドウが表示されたら、確認ボタンを押すとグループ登録が完了します。

 
<br />

## 8. ホストの削除、終了、ネットワーク隔離/解除

- 必要に応じてホストの削除も可能です。 ホストリストの左側にあるチェックボックスにチェックすると現れる '削除' ボタンをクリックすると、そのホストが削除されます。
- PLURA V5 サーバーとの通信が正常な時に削除すると、そのホストにインストールされたエージェントも削除されます。  
 [![image](/docs/images/Manual/siem/system/ja/14.PNG){: width="800" }](/docs/images/Manual/siem/system/ja/14.PNG){: target="_blank"} 

- チェックボックスを選択した後、ホストを終了またはネットワーク隔離/解除することができます。
 [![image](/docs/images/Manual/siem/system/ja/15.PNG){: width="800" }](/docs/images/Manual/siem/system/ja/15.PNG){: target="_blank"} 

<br />

## 9. 協議されたネットワークログ収集登録

- 協議されたネットワークログ収集登録はPublic-Syslogサービスで、エージェントをインストールできない環境のSyslogを収集できるサービスです。
 [![image](/docs/images/Manual/siem/system/ja/16.PNG){: width="800" }](/docs/images/Manual/siem/system/ja/16.PNG){: target="_blank"} 

- IPアドレス入力の場合、外部に通信するIPアドレスを入力してください。
- 整列コード : アップロードされるログのプログラム名がない場合、整列コード可否設定で任意のプログラム名を生成してmsg整列することができます。デフォルトはOFFであり、必要に応じてキュービットセキュリティと協議して修正が必要です。
- すべての情報を登録した後、キュービットセキュリティにご連絡いただければ対応させて頂きます。
