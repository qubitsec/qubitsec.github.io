---
title: 設定
permalink: ja_defense_setting_waf.html
sidebar: M_WAF_ja
topnav: topnav_ja
---

     リアルタイムでハッキングログを検出して攻撃者から防御出来るように設定するページです。
     防御 > 設定 > ウェブファイアウォールでアカウント奪取ブロック/ アカウント奪取制限 / データ流出ブロック / OWASPブロックサービスを 使用出来ます。
     アカウント奪取, データ流出フィルタ使用後、 ブロックサービス可能 (但し, ウェブファイアウォールライセンス使用時)

<br />

## 1. ウェブファイアウォール設定

- 分類
    - ユーザーが防御しようとする分類形式を選択します。
- 例外条件
    - 例外条件に登録されたIPは防御出来ません。
- 動作
    - 防御状態のON/OFFで該当攻撃に対する防御を実行又は解除します。
- トラフィック制限
    - トラフィック制限に対する設定ができます
    - アカウント奪取フィルタに登録されたホスト/パスを対象に動作します。
    - rate, burst値は管理 > ウェブファイアウォール > Group > 制限 > トラフィック制限内の設定値と同期化
- 試し応答認証
    - 試し応答認証に対する設定ができます。
    - アカウント奪取フィルタに登録されたホスト/パスを対象に動作します。
    - ウェブファイアウォール設定に登録されたグループが表示されます。

<br />

- アカウント奪取ブロック   
[![image](/docs/images/Manual/waf/defense/setting/1.png){: width="800" }](/docs/images/Manual/waf/defense/setting/1.png){: target="_blank"}

<br />

- アカウント奪取制限   
[![image](/docs/images/Manual/waf/defense/setting/2.png){: width="800" }](/docs/images/Manual/waf/defense/setting/2.png){: target="_blank"}

<br />

- データ流出ブロック
[![image](/docs/images/Manual/waf/defense/setting/3.png){: width="800" }](/docs/images/Manual/waf/defense/setting/3.png){: target="_blank"}

<br />

- OWASPブロック   
[![image](/docs/images/Manual/waf/defense/setting/4.png){: width="800" }](/docs/images/Manual/waf/defense/setting/4.png){: target="_blank"}
