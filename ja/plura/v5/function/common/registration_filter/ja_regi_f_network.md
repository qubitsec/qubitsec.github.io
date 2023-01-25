---
title: ネットワーク
permalink: ja_regi_f_network.html
sidebar: M_C_ja
topnav: topnav_ja
---

     PLURA V5で収集しているネットワークの全ログを活用し、
     ユーザーがシステムフィルタをカスタマイズ出来ます。

     フィルタ登録サポート対象
     1) Firewall - juniper, secui
     2) IPS - Snipe, sonicawall, fortigate
     3) WAF - baracuda, webfront-k
     4) Switch - cisco, huawei
     5) VPN - secuway
     * 引き続きサポート拡大中


## ネットワークフィルタ登録

[![image](/docs/images/Manual/common/regi/network/1.png){: width="800" }](/docs/images/Manual/common/regi/network/1.png){: target="_blank"}


カスタマイズフィルタ登録DEMO : [https://qubitsec.github.io/ja_filter_registration.html](https://qubitsec.github.io/ja_filter_registration.html){: target="_blank"}

<br />

### 1. メニュー位置
- PLURA V5ウェブページ左ナビゲーションバーメニューのフィルタ > フィルタ登録クリック
[![image](/docs/images/Manual/common/regi/network/2.png)](/docs/images/Manual/common/regi/network/2.png){: target="_blank"}

<br />

### 2. 登録ボタンクリック

[![image](/docs/images/Manual/common/regi/network/3.png){: width="800" }](/docs/images/Manual/common/regi/network/3.png){: target="_blank"}

<br />

### 3. フィルタ分類選択

[![image](/docs/images/Manual/common/regi/network/4.png){: width="800" }](/docs/images/Manual/common/regi/network/4.png){: target="_blank"}

<br />

### 4. システムグループ選択

<br />

### 5. オペレーション選択

<br />

### 6. チャンネル選択

[![image](/docs/images/Manual/common/regi/network/5.png){: width="800" }](/docs/images/Manual/common/regi/network/5.png){: target="_blank"}

<br />

### 7. フィルタ名入力

<br />

### 8. フィルタ説明入力

<br />

### 9. フィルタ危険度(高/中/低)指定

<br />

### 10. フィルタ動作時間(24時間/時間設定)設定

<br />

[![image](/docs/images/Manual/common/regi/network/6.png){: width="800" }](/docs/images/Manual/common/regi/network/6.png){: target="_blank"}

- 例えば退勤以後から出勤までのフィルタ動作を確認したい場合、 “時間設定” 選択後, 確認したい時間を入力します。

<br />

### 11. 動作設定

- 下段の情報入力エリアの追加ボタンをクリックするとデータ値を入力して該当値を含め又は除外出来ます。

- フィルタを登録する時、過検/誤検が発生する可能性があるので担当者と確認後、登録することをお勧めします。

- ネットワークフィルタを登録する時、分類をetc.に選択する必要があります。

- システムグループ登録例

[![image](/docs/images/Manual/common/regi/network/7.png){: width="800" }](/docs/images/Manual/common/regi/network/7.png){: target="_blank"}


 