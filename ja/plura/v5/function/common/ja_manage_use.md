---
title: 使用
permalink: ja_manage_use.html
sidebar: M_C_ja
topnav: topnav_ja
---

- 使用:データ流出設定、Web個人情報の非表示、Web検出例外設定、Web/システム/アプリケーション/ネットワークアップロード設定ができます。
- PLURA V5 Forensic 製品ではデータ流出設定、ウェブ/システムアップロード設定機能をサポートしていません。

[![image](/docs/images/Manual/common/manage/use/1.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />

## 1. 例）pwdに対する値を非表示に設定する
- ウェブ個人情報の非表示:ウェブログを使用する際、個人情報の非表示設定が可能で、設定するとその情報を*で表示します。
- 以下のように、pwd値がそのまま表示しているウェブログを例に挙げて非表示設定をしてみましょう。

[![image](/docs/images/Manual/common/manage/use/2.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />

### 1-1. 管理 > 使用 > ウェブ個人情報非表示 > 設定ボタンをクリックします。
[![image](/docs/images/Manual/common/manage/use/3.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />

### 1-2. 非表示にしたい個人情報を追加します。   
[![image](/docs/images/Manual/common/manage/use/4.png)](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />

### 1-3. 個人情報非表示設定が正常に適用されたことを確認できます。   
[![image](/docs/images/Manual/common/manage/use/5.png)](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

- ウェブ検知例外:全体ログには掲載されますが、検知ログには掲載されないように設定できます。
   - 例）hostアドレスが123.34.45.1のログは検出されないように設定したい場合はhost選択後123.34.45.1を記入してください。
- 管理 > 使用 > ウェブ検知例外 > 例外設定の追加選択   
[![image](/docs/images/Manual/common/manage/use/6.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}
 
<br />

- グループで+に追加する項目はAND条件、グループ間ではOR条件です。   
[![image](/docs/images/Manual/common/manage/use/7.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />

- ウェブアップロード:ユーザーが希望するウェブアップロード形式を選別または例外処理できます。
- ウェブアップロード設定の場合、基本的な画像などのデフォルト設定がされており、ユーザーによって修正が可能です。 
[![image](/docs/images/Manual/common/manage/use/8.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />

[참고] ウェブアップロードDefault設定値   

     Extension : 
     (?i)^(jpg|gif|png|jpeg|ico|bmp|tiff|exif|ppm|pgm|pbm|pnm|mng|pgf|tga|bpg|cgm|svg|hevc|wmv|Xvid|VP6|VP7|VP8|VP9|MPEG-1|MPEF-2|MPEF-4|ACC|mp4|avi|asf|wav|otf|woff|woff2|eot|ttf|less|js|css)$

     Req-Content Type : 
     (?i)(image|video|audio|font)

<br />

- システムアップロード:ユーザーが希望するシステムアップロード形式をOS別に選別または例外処理することができます。   
[![image](/docs/images/Manual/common/manage/use/9.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />

## 2. ウィンドウエージェントイベントチャンネルのログ収集をON/OFFすることができます。

- 設定OFFの場合、そのチャンネルのログ収集は行いません。

### 2-1. パス
C:\ → Program Files(x86) → PLURA → メモ帳(又は Notepad++)で @ELC_config.ini ファイル実行(管理者 権限)

[![image](/docs/images/Manual/common/manage/use/10.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />

### 2-2. 設定値の追加

@ELC_config.ini 設定値追加ファイルを管理者権限で実行した後、以下の設定値を追加します。
- on（チャネルログ収集の有効化）、off（チャネルログ収集の無効化）

     [EVENTLOG]

     DEFAULT=off
     SECURITY=off
     ETC=on

<br />

- DEFAULT Channel : Application, System, Setup, Sysmon log
- SECURITY Channel : Security log
- ETC : DEFAULT, SECURITY Channel ログを除くすべてのログ

[![image](/docs/images/Manual/common/manage/use/11.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}
 
<br />

- アプリケーションのアップロード:ユーザーが希望するアプリケーションログを選別/例外処理できます。   
[![image](/docs/images/Manual/common/manage/use/12.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

## 3. アプリケーションアップロード例外

### 3-1. アプリケーションアップロード例外

- 元のログのうち空白を例外したい場合   
{ “timegenerated”: “2022-05-21T13:20:45.098193+09:00”, “tag”: “top”, “path”: “/var/log/pluraagent.txt”, “msg”: “” }

- 空白が1回以上の時は、 > ^\s+$

- 空白が0回以上の時は、 > ^\s*$

<br />

例示イメージ)

[![image](/docs/images/Manual/common/manage/use/13.png)](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />

### 3-2.  アプリケーションユーザー定義例外 
- 表示したいカスタム エントリを設定します。
- 選択した項目のみがダッシュボード、フルログ、フィルタ検出、レポート メニューから表示されます。

[![image](/docs/images/Manual/common/manage/use/14.png)](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />

## 4. ネットワークアップロード例外
- ユーザーが希望するネットワークログを選別/例外処理することができます。   
[![image](/docs/images/Manual/common/manage/use/15.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />

[関連 ブログ]

- Video > 機能紹介 > SIEM > アップロード設定 DEMO : [https://qubitsec.github.io/ja_upload_setting.html](https://qubitsec.github.io/ja_upload_setting.html){: target="_blank"}