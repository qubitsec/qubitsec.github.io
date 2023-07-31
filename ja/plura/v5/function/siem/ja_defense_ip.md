---
title: ブロックIPアドレス
permalink: ja_defense_ip.html
sidebar: M_SIEM_ja
topnav: topnav_ja
---

     リアルタイムでブロックされたIPアドレスを表示し、直接ブロックしたいIPアドレスを登録したり編集できるページです。

     システムログ照会の下段にある「直ちにブロック」ボタンでブロックIPアドレスに登録して管理することができます。
     ブロックIPアドレスに登録されるとブロックされ、削除するとブロックが解除されます。

     Linuxシステムの場合、Firewalldが活性化されている環境で動作します。

     ▣ 防御登録方法
     1. 全体ログ/検知ログページ > 直ちに防御ボタンをクリック
     2. 防御 > ブロックIPアドレス > システム > IPアドレス登録ボタンをクリック
     3. 防御 > 設定 > システム > 防御設定

<br />

## ブロックIPアドレス > システム
- システムフィルタ検知/全体ログページで直ちに防御ボタンをクリックし、登録した情報またはIPアドレス登録ボタンをクリックして直接登録した情報が表示されます。    
<!-- [![image](/docs/images/Manual/siem/blockIP/1.png){: width="800" }](/docs/images/Manual/siem/blockIP/1.png){: target="_blank"}-->

<br />

- 修正/削除ボタンを通じて編集が可能です。
<!-- [![image](/docs/images/Manual/siem/blockIP/3.png)](/docs/images/Manual/siem/blockIP/3.png){: target="_blank"}-->

<br />

- IPアドレス登録ボタンをクリックすると、下記の設定ポップアップが表示されます。
<!-- [![image](/docs/images/Manual/siem/blockIP/2.png)](/docs/images/Manual/siem/blockIP/2.png){: target="_blank"}-->
- システム:防御対象システムの選択
- IPアドレス : ブロックIPアドレス入力
- 説明:ブロックする理由または目的入力
