---
title: 公開鍵ログインの成功
permalink: ja_public_key_user_registration_method.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

**PLURA V5 > フィルタ > 登録 > システム**

<!-- [![image](/docs/images/Additianal/public_key/1.png){: width="800" }](/docs/images/Additianal/public_key/1.png){: target="_blank"}-->

- オペレーショングループ : linux
- オペレーション : ubuntu or centos (該当するオペレーション選択)
- チャンネル : Syslog
- フィルタ名 : 公開鍵ログインの成功
- フィルタ説明 : 公開鍵ログインの成功時、発行されるログです。
- フィルタリスク : 高
- フィルタ動作時間 : 24時間
- フィルタ状態 : ON

<br />

**デフォルト登録情報**

- 情報入力 > msg > 直接入力 : Accepted publickey for > 含め

 
<br />

**内部IPアドレス除外処理に必要な情報**

- 情報入力 > msg > 直接入力 : Accepted publickey for > 含め
- 情報入力 > msg > 選択入力 : default > 除外
- default: サーバーグループに, defaultへ登録されているIPアドレス検出除外処理