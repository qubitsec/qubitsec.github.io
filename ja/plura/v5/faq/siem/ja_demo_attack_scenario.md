---
title: デモ攻撃シナリオ 
permalink: ja_demo_attack_scenario.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

    PLURA V5を使用するご利用のお客様又はパートナー様が簡単なコマンド実行で検出ログを発生させることができます。

### マイターアタック&相関分析&システム

**PLURA V5エージェントがインストールされたLinux環境で下のコマンドを実行するとマイターアタックとシステム検出ログを確認出来ます。**

``# useradd Demo``

[![image](/docs/images/Additianal/demoattack/01.png)](/docs/images/Additianal/demoattack/01.png){: target="_blank"}

<br />

PLURA V5フィルタ検出 > システムメニューで検出

[![image](/docs/images/Additianal/demoattack/02.png){: width="800" }](/docs/images/Additianal/demoattack/02.png){: target="_blank"}

<br />

``# userdel Demo``

[![image](/docs/images/Additianal/demoattack/03.png)](/docs/images/Additianal/demoattack/03.png){: target="_blank"}

<br />

PLURA V5フィルタ検出 > システムメニューで検出

[![image](/docs/images/Additianal/demoattack/04.png){: width="800" }](/docs/images/Additianal/demoattack/04.png){: target="_blank"}

<br />

PLURA V5 セキュリティ検出 > マイターアタック > リストで検出

[![image](/docs/images/Additianal/demoattack/05.png){: width="800" }](/docs/images/Additianal/demoattack/05.png){: target="_blank"}

<br />

**相関分析検出の場合, 事前に相関分析フィルタが登録されている必要があります。**

※ 相関分析検出サンプル

(パス : フィルタ > セキュリティ > 相関分析 > フィルタ登録)

- 相関分析情報(分流, フィルタ名, 説明など)を入力

- 相関分析Group追加ボタンクリック

- システム/ウェブフィルタ追加ボタンクリック

下のフィルタの場合, システム単一フィルタ追加 “オペレーション : centos, フィルタ名 : アカウント生成(M5919j9igmyqbg9h)&アカウント削除”

[![image](/docs/images/Additianal/demoattack/06.png){: width="800" }](/docs/images/Additianal/demoattack/06.png){: target="_blank"}

<br />

下のコマンドを順番に入力してアカウント生成及び削除フィルタで組み合わせた相関分析フィルタを検出します。

``# useradd Demo``

[![image](/docs/images/Additianal/demoattack/07.png)](/docs/images/Additianal/demoattack/07.png){: target="_blank"}

<br />

``# userdel Demo``

[![image](/docs/images/Additianal/demoattack/08.png)](/docs/images/Additianal/demoattack/08.png){: target="_blank"}

<br />

PLURA V5 セキュリティ検出 > 相関分析メニューで検出

[![image](/docs/images/Additianal/demoattack/09.png){: width="800" }](/docs/images/Additianal/demoattack/09.png){: target="_blank"}

<br /> 

### ウェブ

**ウェブフィルタ検出を環境するためにはデモ攻撃をするウェブサーバ環境が必要です。**

<br />

PLURA V5エージェントがインストールされているウェブサーバ環境にWordpressをインストール, 下の模擬攻撃コマンドをウェブブラウザに入力します。

``?<script>alert("xss")</script>``

<br />

[![image](/docs/images/Additianal/demoattack/10.png)](/docs/images/Additianal/demoattack/10.png){: target="_blank"}

<br />

PLURA V5 フィルタ検出 > ウェブメニューで検出

[![image](/docs/images/Additianal/demoattack/11.png){: width="800" }](/docs/images/Additianal/demoattack/11.png){: target="_blank"}

<br /> 

### ホームページ偽造

**下の説明を参考して多様なオペレーション(CentOS, ubuntu, Windows)でユーザーのホームページフィルタ名(パス)を追加して, ホームページ偽造を 検出出来ます。**

内部ブログ : [ホームページ偽造](https://qubitsec.github.io/ja_s_f_h_forgery.html){: target="_blank"}

1.[エージェントがインストールされているウィンドウ環境] C:\ パスに任意のフォルダ(C:\000)生成
  
[![image](/docs/images/Additianal/demoattack/12.png)](/docs/images/Additianal/demoattack/12.png){: target="_blank"}

<br />

2.[PLURAページ] フィルタ > セキュリティ > ホームページ偽造 > ウィンドウ > ファイルパス(C:\000)追加
  
[![image](/docs/images/Additianal/demoattack/13.png){: width="800" }](/docs/images/Additianal/demoattack/13.png){: target="_blank"}

<br />

3.[エージェントがインストールされているウィンドウ環境] 任意で生成したフォルダ内でtxtファイル生成後, 修正及び削除
  
[![image](/docs/images/Additianal/demoattack/14.png)](/docs/images/Additianal/demoattack/14.png){: target="_blank"}

<br />

4.PLURA V5 セキュリティ検出 > ホームページ偽造メニューで検出
  
[![image](/docs/images/Additianal/demoattack/15.png){: width="800" }](/docs/images/Additianal/demoattack/15.png){: target="_blank"}

<br />

### データ流出 & アカウント奪取

- **データ流出 : 脆弱なウェブサーバ環境で実際データ流出攻撃が発生した場合, 検出出来ます。**

- **アカウント奪取 : 収集されたログを基に分析して, アカウント奪取フィルタを登録する必要があります。**