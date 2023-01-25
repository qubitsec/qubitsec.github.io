---
title: 管理>ウェブファイアウォール
permalink: ja_web_firewall_waf.html
sidebar: M_WAF_ja
topnav: topnav_ja
---

<br />

- システム グループごとにWebファイアウォールの設定を進めることができます。 
 [![image](/docs/images/Manual/waf/firewall/1.png){: width="800" }](/docs/images/Manual/waf/firewall/1.png){: target="_blank"}

<br />

- <グループの追加> ボタンをクリックして、システム グループを追加できます。
 [![image](/docs/images/Manual/waf/firewall/2.png)](/docs/images/Manual/waf/firewall/2.png){: target="_blank"}

<br />

- システム グループごとにWebファイアウォールのお知らせ設定を進めることができます。 
  - 接続例外設定により点検中例外処理(IPアドレス登録)が可能です。

  [![image](/docs/images/Manual/waf/firewall/9.png){: width="800" }](/docs/images/Manual/waf/firewall/9.png){: target="_blank"}

<br />

- ウェブファイアウォールのお知らせ設定 > プレビューボタンをクリックして作成した内容を確認することができます。
 [![image](/docs/images/Manual/waf/firewall/10.png){: width="800" }](/docs/images/Manual/waf/firewall/10.png){: target="_blank"}

<br />

- システム グループごとにWebファイアウォールのブロック案内設定を進めることができます。
 [![image](/docs/images/Manual/waf/firewall/11.png){: width="800" }](/docs/images/Manual/waf/firewall/11.png){: target="_blank"}

<br />

- 運用方式:該当グループのウェブファイアウォールの運用方式を検知/遮断中に設定することができます。
 [![image](/docs/images/Manual/waf/firewall/3.png)](/docs/images/Manual/waf/firewall/3.png){: target="_blank"}

<br />

- X-Forwarded-For : 入力/出力を設定できます。 
 [![image](/docs/images/Manual/waf/firewall/4.png)](/docs/images/Manual/waf/firewall/4.png){: target="_blank"}

<br />

- Proxy : Proxy設定（ウェブファイアウォールSSL、ホストなど）ができます。

<br />

- <ホスト> を読み込む:管理 > リスト > ホストに登録した情報を取得できます。
 [![image](/docs/images/Manual/waf/firewall/5.png){: width="800" }](/docs/images/Manual/waf/firewall/5.png){: target="_blank"}
 
<br />

- アクセス制限ONする場合、IPアドレスとGeoIP設定を管理者が直接設定できます。

- GeoIPの場合、チェックボックスを選択した国でのみアクセス(Whitelist)が可能です。
  [![image](/docs/images/Manual/waf/firewall/6.png){: width="800" }](/docs/images/Manual/waf/firewall/6.png){: target="_blank"}

<br />

- アクセス制限 > IPアドレス > "登録" ボタンをクリックすると、特定のIP接続に対する許可/遮断設定ができます。  
  [![image](/docs/images/Manual/waf/firewall/7.png)](/docs/images/Manual/waf/firewall/7.png){: target="_blank"}

<br />

- 制限:トラフィック制限、試行応答認証、スケジュール変更により、Webファイアウォールの制限設定ができます。

- アカウント乗っ取りフィルタに登録されたホスト/パスがないと設定できません。   
 [![image](/docs/images/Manual/waf/firewall/8.png){: width="800" }](/docs/images/Manual/waf/firewall/8.png){: target="_blank"}