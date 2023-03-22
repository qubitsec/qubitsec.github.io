---
title: ダッシュボード
permalink: ja_dash_board.html
sidebar: M_SIEM_ja
topnav: topnav_ja
---

     リアルタイムでハッキングログを検知し、視覚化で表示するページです。
     ダッシュボードに表示されるすべてのログは、まずフィルタページでフィルタ登録をしなければなりません。

<br />

ダッシュボードの上部には、検出件数/登録システム/検出ログ発生システム数/ログ未アップロードシステム数/ログアップロード量/リソースモニタリングが表示されます。

<!-- [![image](/docs/images/Manual/siem/dash/1.png){: width="800" }](/docs/images/Manual/siem/dash/1.png){: target="_blank"}-->

<br />

- そのシステムの数をクリックすると、システム管理ページに移動します。 
<!-- [![image](/docs/images/Manual/siem/dash/2.png)](/docs/images/Manual/siem/dash/2.png){: target="_blank"}-->

- 1 時間以内にログ発生がない場合、シスログ/ウェブログ未アップロードシステム項目に表示されます。
<!-- [![image](/docs/images/Manual/siem/dash/3.png){: width="800" }](/docs/images/Manual/siem/dash/3.png){: target="_blank"}-->

<br />

その下にはマイターアタック/相関分析/データ流出/アカウント奪取/システム/アプリケーション/ウェブ/ネットワークで検出されたログの数を示します。

<br />

## 1. リアルタイム検出項目

- マイターアタック/相関分析/データ流出/アカウント奪取/システム/アプリケーション/Web/ネットワーク
- 該当ログを選択すると、以下の項目が表示されます。 
<!-- [![image](/docs/images/Manual/siem/dash/4.png){: width="800" }](/docs/images/Manual/siem/dash/4.png){: target="_blank"}-->

- 最近検出されたログ
- 検知フィルタ TOP 5
- 危険度別ログ発生状況
- 時間別ログ発生状況
- 接続IPTOP5
- 検知ログサーバーTOP5

<br />

- 最近検出されたログの <詳細> をクリックすると、その検出ログ ページに移動します。
<!-- [![image](/docs/images/Manual/siem/dash/5.png)](/docs/images/Manual/siem/dash/5.png){: target="_blank"}-->
<!-- [![image](/docs/images/Manual/siem/dash/6.png){: width="800" }](/docs/images/Manual/siem/dash/6.png){: target="_blank"}-->

<br />

## 2. 時間別ログ発生状況

- 前日発生グラフと比較して検知ライングラフを確認することができます。 
<!-- [![image](/docs/images/Manual/siem/dash/7.png){: width="800" }](/docs/images/Manual/siem/dash/7.png){: target="_blank"}-->

<br />

## 3. 画面設定

- ダッシュボードの右側の歯車をクリックすると、画面設定ページが表示されます。 
<!-- [![image](/docs/images/Manual/siem/dash/8.png){: width="800" }](/docs/images/Manual/siem/dash/8.png){: target="_blank"}-->   
<!-- [![image](/docs/images/Manual/siem/dash/9.png){: width="800" }](/docs/images/Manual/siem/dash/9.png){: target="_blank"}-->

 <br />

+ グループ設定
   - ダッシュボードに表示するシステム グループの設定
   - 上部領域表示
   - 上部に表示する領域設定
   - デフォルトメニュー
   - ダッシュボードに接続すると見えるログ
   - メニュー表示設定
   - ユーザーが希望するログのみダッシュボードに表示
   - パーソナルダッシュボード使用
   - ユーザーカスタムダッシュボード機能の使用設定
   - 初期化
   - デフォルトメニューは相関分析
   - メニュー表示設定は全体に設定されます。

<br />

## 4. パーソナルダッシュボード

- ユーザーが希望するフィルタを設定して監視できます。
<!-- [![image](/docs/images/Manual/siem/dash/10.png){: width="800" }](/docs/images/Manual/siem/dash/10.png){: target="_blank"}-->   
<!-- [![image](/docs/images/Manual/siem/dash/11.png){: width="800" }](/docs/images/Manual/siem/dash/11.png){: target="_blank"}-->

 참고영상 : PLURA V5ダッシュボード/メニュー活用   
 [https://qubitsec.github.io/ja_dash_menu.html](https://qubitsec.github.io/ja_dash_menu.html){: target="_blank"}