---
title: アカウント乗っ取り
permalink: ja_s_f_acc_takeover.html
sidebar: M_C_ja
topnav: topnav_ja
---

     アカウント乗っ取りセキュリティフィルタにはクレデンシャルスタッフィング(Credential Stuffing)、 ボリューム型（Volumetric）があります。

<br />

▶ クレデンシャルスタッフィング(Credential Stuffing)とは?
[https://owasp.org/www-community/attacks/Credential_stuffing](https://owasp.org/www-community/attacks/Credential_stuffing){: target="_blank"}

セキュリティフィルタのうち、クレデンシャルスタッフィング(Credential Stuffing)は様々なログインの試みを通じてアカウントを奪取する攻撃を検知するフィルタです。

▶ ボリューム型（Volumetric）とは？
[https://www.a10networks.com/blog/understanding-ddos-attacks/](https://www.a10networks.com/blog/understanding-ddos-attacks/){: target="_blank"}

セキュリティフィルタのうち、ボリューム型（Volumetric）はランダムな代入によるアカウント乗っ取り攻撃を検出するフィルタです。

<br />

<!-- [![image](/docs/images/Manual/common/filter2/security/takeover/1.png){: width="800" }](/docs/images/Manual/common/filter2/security/takeover/1.png){: target="_blank"}-->

- 分類 : ボリューム型(固定), ボリューム型(可変), クレデンシャルスタッフィング(固定), クレデンシャルスタッフィング(可変) の中を選択することができます。
- フィルタ名 : フィルタ名を入力します。 検知ログに表示する情報で簡単に調べられる名前に決めます。
- ホスト : ホスト情報を入力します。
- マルチホスト登録が可能です。
- ホスト登録は管理 > リスト > ホストメニューから管理者が登録できます。
（運営者、モニタリング権限ではホストメニューの非表示（Hidden）処理）
- パス : パス（ログインページ）を入力します。
- メソッド(Method) : POST、GETの中から選択します。
- ログイン属性 : nameを入力します。
- 時間帯 : 設定した時間にフィルタが動作します。
- 動作 : フィルタの使用有無を選択します。
- Login成功/失敗 : Login成功/失敗を選択します。
- ステータス値 : Statusを選択します。
- 応答サイズ : 応答サイズはステータス値表記のための条件で、PLURA V5で収集された全体ログ情報を通じて応答サイズを確認して入力します。
応答サイズを除外したい場合は、応答サイズのチェックボックスを解除します。
- 試行回数/条件/使用ID数 : 検出条件(試行回数/条件/使用ID数)を入力します。
AND、OR条件を活用できます。

<br />

以下は登録例です 

<!-- [![image](/docs/images/Manual/common/filter2/security/takeover/2.png){: width="800" }](/docs/images/Manual/common/filter2/security/takeover/2.png){: target="_blank"}-->