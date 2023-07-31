---
title: Estatik plugin vulnerability
permalink: ja_Estatik_plugin.html
sidebar: Video_HD_testing_ja
topnav: topnav_ja
---

<!-- <style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/fNhVYHjSKdQ' frameborder='0' allowfullscreen></iframe></div> -->

<br />

## 1. Estatik plugin vulnerability

ワードプレス Estatik pluginは、 動産ウェブサイトを構成できるプラグインです。

2.2.1バージョンにアップロード関数でファイル拡張子チェックをするロジックが存在せず、ワードプレスが提供するAjaxの誤った使用によりファイルアップロードの脆弱性が発生しました。

<br />

## 2. 模擬攻撃シナリオ

  1) Estatik plugin 脆弱性を利用したファイルアップロード攻撃

  2) 攻撃ログがPLURAで正常に収集されたか確認

  3) PLURAウェブファイアウォールログを活用した分析方法

  4) PLURAウェブファイアウォール(WAF)- Estatik plugin脆弱性攻撃に対するブロック試演

<br />

## 3. 参考サイト
  
  [1] ワードプレスで作成したサイトの必須セキュリティ TOP 10 [http://blog.plura.io/?p=18623](http://blog.plura.io/?p=18623){: target="_blank"}

  