---
title: エージェント削除
permalink: ja_agent_uninstall.html
sidebar: faq_common_M_ja
topnav: topnav_ja
---

<br />

### 1. Windowsエージェント

<br />

#### 1-1. パス移動

設定 > プログラム > プログラム及び機能 > プログラム削除及び変更>に移動してください。

<br />

#### 1-2. PLURA削除/変更クリック

[![image](/docs/images/Faq/Agent/ja_03.png)](/docs/images/Faq/Agent/ja_03.png){: target="_blank"}

<br />

#### 1-3. PLURA削除

PLURA削除ポップアップが出ると<はい>をクリックしてください。

<!-- [![image](/docs/images/Faq/Agent/ja_04.png)](/docs/images/Faq/Agent/ja_04.png){: target="_blank"} -->

<br />

#### 1-4. ウェブログモジュール削除

ウェブログ収集を解除して, ウェブログモジュールを削除したいユーザーの場合は＜ウェブログ設定 > ウェブログモジュール削除＞ ボタンで削除してください。

[![image](/docs/images/Faq/Agent/ja_05.png)](/docs/images/Faq/Agent/ja_05.png){: target="_blank"}

<br />

### 2. Linuxエージェント

LinuxでPLURA V5 Agent削除する方法です。

下のCommandを実行するとPLURA V5 Agentに対する全てのモジュールが削除されます。

<br />

#### 2-1. CentOS/RHEL/Ubuntu Agent削除

``# /etc/plura/plura.sh uninstall``
