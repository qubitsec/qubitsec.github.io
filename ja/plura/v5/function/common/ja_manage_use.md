---
title: 使用
permalink: ja_manage_use.html
sidebar: M_C_ja
topnav: topnav_ja
---

- 使用:データ流出設定、Web個人情報の非表示、Web検出例外設定、Web/システム/アプリケーション/ネットワークアップロード設定ができます。
- PLURA V5 Forensic 製品ではデータ流出設定、ウェブ/システムアップロード設定機能をサポートしていません。

 [![image](/docs/images/Manual/common/manage/use/ja/1.PNG)](/docs/images/Manual/common/manage/use/ja/1.PNG){: target="_blank"}

<br />

## 1. ウェブアップロードの例外
- ウェブ個人情報の非表示:ウェブログを使用する際、個人情報の非表示設定が可能で、設定するとその情報を*で表示します。
- 以下のように、pwd値がそのまま表示しているウェブログを例に挙げて非表示設定をしてみましょう。

 [![image](/docs/images/Manual/common/manage/use/ja/2.PNG)](/docs/images/Manual/common/manage/use/ja/2.PNG){: target="_blank"}

<br />

### 1-1. 管理 > 使用 > ウェブ個人情報非表示 > 設定ボタンをクリックします。
 [![image](/docs/images/Manual/common/manage/use/ja/3.PNG)](/docs/images/Manual/common/manage/use/ja/3.PNG){: target="_blank"}

<br />

### 1-2. 非表示にしたい個人情報を追加します。   
 [![image](/docs/images/Manual/common/manage/use/ja/4.PNG)](/docs/images/Manual/common/manage/use/ja/4.PNG){: target="_blank"}

<br />

### 1-3. 個人情報非表示設定が正常に適用されたことを確認できます。   
 [![image](/docs/images/Manual/common/manage/use/ja/5.PNG)](/docs/images/Manual/common/manage/use/ja/5.PNG){: target="_blank"}

- ウェブ検知例外:全体ログには掲載されますが、検知ログには掲載されないように設定できます。
   - 例）hostアドレスが123.34.45.1のログは検出されないように設定したい場合はhost選択後123.34.45.1を記入してください。
- 管理 > 使用 > ウェブ検知例外 > 例外設定の追加選択   
 [![image](/docs/images/Manual/common/manage/use/ja/6.PNG){: width="800" }](/docs/images/Manual/common/manage/use/ja/6.PNG){: target="_blank"}
 
<br />

- アカウント乗っ取り例外設定も上記の説明と同じ方法でアカウント乗っ取り検出ログで例外処理が可能です。

  ※ アカウント乗っ取り例外設定の場合、ログ量によって設定情報が適用されるのに最低10分の時間がかかります。

- グループで+に追加する項目はAND条件、グループ間ではOR条件です。   
 [![image](/docs/images/Manual/common/manage/use/ja/7.PNG){: width="800" }](/docs/images/Manual/common/manage/use/ja/7.PNG){: target="_blank"}

<br />

- ウェブアップロード:ユーザーが希望するウェブアップロード形式を選別または例外処理できます。
- ウェブアップロード設定の場合、基本的な画像などのデフォルト設定がされており、ユーザーによって修正が可能です。 
 [![image](/docs/images/Manual/common/manage/use/ja/8.PNG){: width="800" }](/docs/images/Manual/common/manage/use/ja/8.PNG){: target="_blank"}

<br />

[参考] ウェブアップロードDefault設定値   

     Extension : 
     (?i)^(jpg|gif|PNG|jpeg|ico|bmp|tiff|exif|ppm|pgm|pbm|pnm|mng|pgf|tga|bpg|cgm|svg|hevc|wmv|Xvid|VP6|VP7|VP8|VP9|MPEG-1|MPEF-2|MPEF-4|ACC|mp4|avi|asf|wav|otf|woff|woff2|eot|ttf|less|js|css)$

     Req-Content Type : 
     (?i)(image|video|audio|font)

<br />

<br />

## 2. ホストアップロードの例外

### 2-1. ホスト終了/ネットワーク隔離
- ホスト終了、ネットワーク隔離メニューの公開設定ができます。
[![image](/docs/images/Manual/common/manage/use/ja/9.PNG)](/docs/images/Manual/common/manage/use/ja/9.PNG){: target="_blank"}

  - メニュー公開設定をした場合、システム > システム管理 > ホストの選択 > セキュリティタブで確認できます。
    - ホスト終了 : ホストの終了を実行します。
    - ネットワーク分離：PLURAエージェントを除くすべてのネットワークを遮断します。

<br />

### 2-2. ホストアップロードの例外

- ホストアップロード : ユーザーが希望するホストログを選別/例外処理することができます。

 [![image](/docs/images/Manual/common/manage/use/ja/10.PNG){: width="800" }](/docs/images/Manual/common/manage/use/ja/10.PNG){: target="_blank"}
 
<br />

  


## 3. アプリケーションアップロード例外
- アプリケーションのアップロード:ユーザーが希望するアプリケーションログを選別/例外処理できます。 
 [![image](/docs/images/Manual/common/manage/use/ja/11.PNG){: width="800" }](/docs/images/Manual/common/manage/use/ja/11.PNG){: target="_blank"}

### 3-1. アプリケーションアップロード例外

- 元のログのうち空白を例外したい場合   
{ “timegenerated”: “2022-05-21T13:20:45.098193+09:00”, “tag”: “top”, “path”: “/var/log/pluraagent.txt”, “msg”: “” }

- 空白が1回以上の時は、 > ^\s+$

- 空白が0回以上の時は、 > ^\s*$

<br />

例示イメージ)

 [![image](/docs/images/Manual/common/manage/use/ja/12.PNG){: width="800" }](/docs/images/Manual/common/manage/use/ja/12.PNG){: target="_blank"}

<br />

### 3-2.  アプリケーションユーザー定義例外 
- 表示したいカスタム エントリを設定します。
- 選択した項目のみがダッシュボード、フルログ、フィルタ検出、レポート メニューから表示されます。

 [![image](/docs/images/Manual/common/manage/use/ja/13.PNG)](/docs/images/Manual/common/manage/use/ja/13.PNG){: target="_blank"}

<br />

## 4. ネットワークアップロード例外
- ユーザーが希望するネットワークログを選別/例外処理することができます。   
 
 [![image](/docs/images/Manual/common/manage/use/ja/14.PNG){: width="800" }](/docs/images/Manual/common/manage/use/ja/14.PNG){: target="_blank"}

<br />

[関連 ブログ]

- Video > 機能紹介 > SIEM > アップロード設定 DEMO : [https://qubitsec.github.io/ja_upload_setting.html](https://qubitsec.github.io/ja_upload_setting.html){: target="_blank"}