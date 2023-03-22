---
title: グループ通知
permalink: ja_manage_group.html
sidebar: M_C_ja
topnav: topnav_ja
---

- グループ通知:PLURA V5通知(検知、防御、エージェント停止)をWebフック設定で受信できます。

- 選択したWebフックのアドレステンプレートが自動入力されます。

- エージェント中止通知はオンプレミス環境専用機能   

<!-- [![image](/docs/images/Manual/common/manage/group/01.png){: width="800" }](/docs/images/Manual/common/manage/group/01.png){: target="_blank"}-->

<br />

## 1. 通知タイプ
- Webフックの発送タイプによって、個別または一括方式の発送タイプにユーザーが設定できます。

<br />

## 2. 代表/グループ別選択可能
- 代表またはサービスグループ別に区分してWebフック通知を受けることができます。

<br />

## 3. 通知詳細選択

<!-- [![image](/docs/images/Manual/common/manage/group/2.png)](/docs/images/Manual/common/manage/group/2.png){: target="_blank"}-->

<br />

- 追加、削除ボタンを使用して、Webフック通知を受信するサーバーの編集を行うことができます。

- 編集ボタンをクリックすると、詳細な通知を選択できるポップアップウィンドウが表示されます。
  - 検知 : マイター、相関分析、データ流出、アカウント乗っ取り、システムログ、ウェブログ、ネットワークログ
  - 防御 : 相関分析、データ流出、アカウント乗っ取り、システムログ、ウェブログ、ネットワークログ  
  - 使用ログ : メンバー、フィルタ、サーバー、防御、顧客サポート、その他   
  - エージェント中止

<!-- [![image](/docs/images/Manual/common/manage/group/3.png)](/docs/images/Manual/common/manage/group/3.png){: target="_blank"}-->

<br />

## 4. 環境情報入力
-  Webフック通知を受けようとする環境のプロトコル、フォーマット形式、サーバーIPアドレス、ポート番号、改行タイプを入力します。

<br />

グループ通知(Webフック)の設定 DEMO : [https://qubitsec.github.io/ja_setting_up_webhook.html](https://qubitsec.github.io/ja_setting_up_webhook.html){: target="_blank"}