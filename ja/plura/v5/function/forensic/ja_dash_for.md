---
title: ダッシュボード
permalink: ja_dash_for.html
sidebar: M_for_ja
topnav: topnav_ja
---

     リアルタイムでハッキングログを検知し、視覚化で表示するページです。
     ダッシュボードに表示されるすべてのログは、まずフィルタページでフィルタ登録をしなければなりません。

<br />

- ダッシュボードの上部では、マイタ/相関分析/システムログで検出されたログの数を示します。

- ライセンス（クラウド基準）ごとのアップロード容量とログ保管期間
   - Standard(LogF) : 300GB , 90日
   - Gold(LogF) : 1TB, 90日
   - Platinum(LogF) : 2TB, 180日

<br />

## 1. リアルタイム検出項目

- マイター / 相関分析 / システムログ
- 該当ログを選択すると、以下の項目が表示されます。   
[![image](/docs/images/Manual/forensic/dash/1.png){: width="800" }](/docs/images/Manual/forensic/dash/1.png){: target="_blank"}

- 年度別ログ発生状況
- 月別ログ発生状況
- 日別発生状況
- マトリックス(マイター)

<br />

## 2. 年度別ログ発生状況
- 選択した検知項目に対する年度別発生グラフを確認することができます。   
[![image](/docs/images/Manual/forensic/dash/2.png){: width="800" }](/docs/images/Manual/forensic/dash/2.png){: target="_blank"}

<br />

## 3. 月別ログ発生状況
- 選択した検出項目の月別発生グラフを確認できます。
[![image](/docs/images/Manual/forensic/dash/3.png){: width="800" }](/docs/images/Manual/forensic/dash/3.png){: target="_blank"}

<br />

## 4. 日替わり対数発生状況
- 前日発生グラフと比較して検知ライングラフを確認することができます。   
[![image](/docs/images/Manual/forensic/dash/4.png){: width="800" }](/docs/images/Manual/forensic/dash/4.png){: target="_blank"}

<br />

## 5. 画面設定
- ダッシュボードの右側の歯車をクリックすると、画面設定ページが表示されます。 
[![image](/docs/images/Manual/forensic/dash/5.png){: width="800" }](/docs/images/Manual/forensic/dash/5.png){: target="_blank"}   
[![image](/docs/images/Manual/forensic/dash/6.png)](/docs/images/Manual/forensic/dash/6.png){: target="_blank"}

### 5-1. グループ設定

- ダッシュボードに表示するシステム グループの設定

### 5-2.デフォルトメニューの設定

- ダッシュボードに接続すると見えるログ

### 5-3. メニュー表示設定

- ユーザーが希望するログのみダッシュボードに表示

### 5-4.初期化

- デフォルトメニューは相関分析
- メニュー表示設定は全体に設定されます。