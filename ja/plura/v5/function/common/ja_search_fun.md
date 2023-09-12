---
title: 検索機能
permalink: ja_search_fun.html
sidebar: M_C_ja
topnav: topnav_ja
---

     ページ別右上のヘルプをクリックすると、各ログについての説明が案内されています。
     文字列、数字別に様々な検索が可能です。

<br />

### 1. 検索方法 簡単TIP

     2019-04-30T06:21:25* : 2019-04-30T-6:21:25で始まるすべての情報検索
     検索追加:AND検索可能
     検索個人化:検索条件の個人化

<br />

### 2. メニュー別検索方法 簡単TIP

     フィルタ検知ページ:フィルタ名、詳細表示xml基準で一部検索可能
     ログ照会ページ:詳細表示xml基準で一部検索可能
     フィルタ管理:イベントタイプ、フィルタ名検索可能
     IPアドレス抽出:IP、国、抽出日検索可能
     システム管理:システムIP、ホスト名、登録日検索可能

     検索機能は、検索窓に検索したい検索語を入力したり、詳細表示のXMLに基づいて希望するフレーズをcopy&pasteして検索することができます。
     以下の方法で検索機能を活用できます。

<br />

### 3. 文字列検索時、"含む"、"一致"、"除く"、"含む"項目を選択できます。

 [![image](/docs/images/Manual/common/search/ja/1.PNG){: width="800" }](/docs/images/Manual/common/search/ja/1.PNG){: target="_blank"}

<br />

### 4. 数字検索項目選択時、演算記号選択が可能です。

 [![image](/docs/images/Manual/common/search/ja/2.PNG){: width="800" }](/docs/images/Manual/common/search/ja/2.PNG){: target="_blank"}

<br />

### 5. 検索条件に対してパーソナライズ設定(適用、未適用、固定)が可能です。

     - Full Logで"wordpress"という文字列が含まれ、logStatus値が200以上のログ検索を固定して使用したい場合は、以下のように検索します。
     - 検索パーソナライズ領域で、固定ボタンを選択します。

<br />

 [![image](/docs/images/Manual/common/search/ja/3.PNG){: width="800" }](/docs/images/Manual/common/search/ja/3.PNG){: target="_blank"}

<br />

### 6. ログ照会時、右マウス動作でリンクを提供

 [![image](/docs/images/Manual/common/search/ja/4.PNG){: width="800" }](/docs/images/Manual/common/search/ja/4.PNG){: target="_blank"}

<br />

### 7. タイマー機能:検索条件が追加される場合、右上にタイマーが表示

 [![image](/docs/images/Manual/common/search/ja/5.PNG){: width="800" }](/docs/images/Manual/common/search/ja/5.PNG){: target="_blank"}

     - 対象ライセンス:Enterprise(On-Prem)、Platinum、Premiumに提供
     - 全体ログ、フィルタ検知、ML検知ページに表示

     - タイマーが終了すると、ページが更新され、データを更新します。
     - 検索時間設定（30s、60s、90s、120s）を変更できます。

<br />

 [![image](/docs/images/Manual/common/search/ja/6.PNG)](/docs/images/Manual/common/search/ja/6.PNG){: target="_blank"}

<br />

### 8. 検索ワード自動完成機能

- セキュリティ検知、フィルタ検知ページで検索対象が「フィルタ名」の場合、自動完成機能を使用することができます。

 [![image](/docs/images/Manual/common/search/ja/7.PNG){: width="600" }](/docs/images/Manual/common/search/ja/7.PNG){: target="_blank"}

<br /> 

- フィルタ検知、全体ログ > システムページで検索対象が"チャンネル"の場合、自動完成機能を使用することができます。

 [![image](/docs/images/Manual/common/search/ja/8.PNG){: width="600" }](/docs/images/Manual/common/search/ja/8.PNG){: target="_blank"}

<br />

- 検索ワードを入力した後、"追加"ボタンをクリックする場合、自動完成機能で検索された検索ワードを選択すると検索が可能になります。

<br />

### 9.  以下は、ログ検索の例です。

     - 応答サイズが10000以上で、logURI値が/wordpress/index.phpであるログ検索を希望する場合は、以下のように検索します。

<br />

 [![image](/docs/images/Manual/common/search/ja/9.PNG){: width="800" }](/docs/images/Manual/common/search/ja/9.PNG){: target="_blank"}

 <br />



 