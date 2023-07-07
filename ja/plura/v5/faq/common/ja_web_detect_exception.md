---
title: ウェブ検知例外を設定したい
permalink: ja_web_detect_exception.html
sidebar: faq_common_M_ja
topnav: topnav_ja
---

<br />

## ウェブ検知例外

<br />

全体ログにはアップされますが、検知ログにはアップされないように設定できます。

例）hostアドレスが123.34.45.1のログを検知できないように設定したい場合はhost選択後123.34.45.1を記入してください。

<br />







### 1. パス移動

管理 > 使用 > ウェブ検知例外 > 例外設定の追加設定

[![image](/docs/images/Faq/Agent/ja_10.png){: width="800" }](/docs/images/Faq/Agent/ja_10.png){: target="_blank"}

<br />

### 2. 情報入力

グループで+として追加する項目はAND条件、グループ間はOR条件です。

[![image](/docs/images/Faq/Agent/ja_11.png)](/docs/images/Faq/Agent/ja_11.png){: target="_blank"}

<br />

内部ブログ

[https://qubitsec.github.io/ja_manage_use.html](https://qubitsec.github.io/ja_manage_use.html){: target="_blank"}
