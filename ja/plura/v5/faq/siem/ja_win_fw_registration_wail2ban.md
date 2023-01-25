---
title: Wail2banによるウィンドウファイアウォール設定
permalink: ja_win_fw_registration_wail2ban.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

     Wail2banを使用してRDP無差別代入攻撃に対するセキュリティ設定をした場合, Wail2banによってウィンドウファイアウォールにブロック登録される動作をPLURA V5で検出出きます。

<br />

Wail2banとは?

[https://developer.ibm.com/kr/cloud/softlayer-bluemix-infra/security/2017/08/31/rdp-security-script/](https://developer.ibm.com/kr/cloud/softlayer-bluemix-infra/security/2017/08/31/rdp-security-script/){: target="_blank"}

<br />

## 1. フィルタ登録例

PLURA V5ウェブのフィルタ登録設定方法

**フィルタ > 登録 > システム > 登録する**

**サーバグループ選択 > オペレーティングシステムwindows選択 > Securityチャンネル選択 > イベントタイプ選択**

[![image](/docs/images/Additianal/wail/1.png){: width="800" }](/docs/images/Additianal/wail/1.png){: target="_blank"}

イベントタイプ選択のファイアウォール例外リスト変更ルール追加(4946)選択

動画のように選択し、‘データ値’にwail2ban blockを入れて下段の‘登録’ボタンをクリック

<br />

## 2. ファイアウォール登録検出例

Wail2banによってウィンドウファイアウォールブロック登録されると下のように検出されます。

ログ例 : フィルタ検出 > システム

[![image](/docs/images/Additianal/wail/2.png){: width="800" }](/docs/images/Additianal/wail/2.png){: target="_blank"}



 