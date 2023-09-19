---
title: 連動
permalink:  ja_manage_peristalsis.html
sidebar: M_C_ja
topnav: topnav_ja
---

- 連動:コンプライアンス修正およびチケット管理、Syslog連動設定ができます。

  [![image](/docs/images/Manual/common/manage/peristalsis/ja/1.PNG){: width="800" }](/docs/images/Manual/common/manage/peristalsis/ja/1.PNG){: target="_blank"}

 <br />

## 1. コンプライアンス
- PCI-DSS_v3.2.1, ISMS-P, ISO27001:2013, 電子金融監督規定への適用及び修正を行うことができます。   
- PLURA V5 Forensic 製品ではサポートされていない機能です。

<br />

## 2. チケット連動設定

- チケット "修正する" ボタンをクリックし、設定できます。   
  [![image](/docs/images/Manual/common/manage/peristalsis/ja/2.PNG){: width="800" }](/docs/images/Manual/common/manage/peristalsis/ja/2.PNG){: target="_blank"}

<br />

- 修正完了後、右下のチケット発行テストボタンで正常連動可否を確認できます。   
  [![image](/docs/images/Manual/common/manage/peristalsis/ja/3.PNG){: width="700" }](/docs/images/Manual/common/manage/peristalsis/ja/3.PNG){: target="_blank"}

<br />

## 3. チケット発行

- チケットの発行を希望するログで右下のチケットボタンをクリックすると、チケットが発行されます。   
  [![image](/docs/images/Manual/common/manage/peristalsis/ja/4.PNG){: width="800" }](/docs/images/Manual/common/manage/peristalsis/ja/4.PNG){: target="_blank"}

<br />

- チケットが発行されると、連動したシステムで内容を確認できます。   
  <!--[![image](/docs/images/Manual/common/manage/peristalsis/ja/5.PNG){: width="800" }](/docs/images/Manual/common/manage/peristalsis/ja/5.PNG){: target="_blank"}-->

- ログ照会ページの上段にある発行チケットボタンをクリックすると、発行チケットページに移動して発行されたチケットに関する情報を確認することができます。  
  <!--[![image](/docs/images/Manual/common/manage/peristalsis/ja/6.PNG){: width="800" }](/docs/images/Manual/common/manage/peristalsis/ja/6.PNG){: target="_blank"}-->

<br />

## 4. Syslog 連動設定

4-1. 代表/グループ別選択可能
- 代表またはサービスグループ別に区分してSyslog通知を受けることができます。

<br />

4-2. 通知詳細選択   
  [![image](/docs/images/Manual/common/manage/peristalsis/ja/7.PNG){: width="800" }](/docs/images/Manual/common/manage/peristalsis/ja/7.PNG){: target="_blank"}

- 追加、削除ボタンを利用してsyslog通知を受けるサーバー編集をすることができます。
- タブ移動（検知、防御、使用ログ）をして設定を変更できます。
- 編集ボタンをクリックすると、詳細な通知を選択できるポップアップ ウィンドウが表示されます。
   - 検出:相関分析、システム、Web、ネットワーク、アカウント乗っ取り、データ流出、マイターアタック、Webファイアウォール、アプリケーション
   - 防御:相関分析、システム、Web、ネットワーク、アカウント乗っ取り、データ流出、Webファイアウォール
   - 使用ログ: メンバー、フィルタ、サーバー、防御、顧客サポート、その他

<br />

4-3. syslog通知を受けようとするサーバーの環境情報入力
- プロトコル、Syslogフォーマット、サーバーIPアドレス、ポート番号、改行タイプを入力します。
- 例_Syslog 設定

  [![image](/docs/images/Manual/common/manage/peristalsis/ja/8.PNG){: width="800" }](/docs/images/Manual/common/manage/peristalsis/ja/8.PNG){: target="_blank"}
