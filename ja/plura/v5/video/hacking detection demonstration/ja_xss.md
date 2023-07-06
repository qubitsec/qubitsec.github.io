---
title: XSS
permalink: ja_xss.html
sidebar: Video_HD_testing_ja
topnav: topnav_ja
---

<!-- <style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/dfbZ6_tWthA' frameborder='0' allowfullscreen></iframe></div> -->

<br />

## 1. クロスサイトスクリプティング(XSS)

ウェブアプリケーションで多く見られる脆弱性の一つとして、ウェブサイト管理者ではなく、人がウェブサイトに悪性スクリプトを挿入できる脆弱性です。

主に複数のユーザーが見る電子掲示板に悪性スクリプトが含まれた文を載せる形で行われます。

この脆弱性は、ウェブアプリケーションがユーザーから入力された値を正しくスキャンせずに使用する場合に現れます。

この脆弱性により、ハッカーがユーザーの情報(クッキー、セッションなど)を奪取したり、自動的に異常な機能を遂行させることができます。

主に他のウェブサイトと情報を交換するように動作するので、クロスサイトスクリプティングといいます。

<br />

## 2. 模擬攻撃シナリオ
  
  1) クロスサイトスクリプティング(XSS) 攻撃実行
  
  2) 攻撃ログがPLURAで正常に収集されたか確認
  
  3) PLURAウェブフィルタを活用した分析方法

<br />

## 3. 参考サイト

  [1] XSS 対応方法 [http://blog.plura.io/?p=7614](http://blog.plura.io/?p=7614){: target="_blank"}

  [2] Q&A掲示板、丁寧に書かれた質問、その裏に隠されたXS攻撃 [http://blog.plura.io/?p=6923](http://blog.plura.io/?p=6923){: target="_blank"}
