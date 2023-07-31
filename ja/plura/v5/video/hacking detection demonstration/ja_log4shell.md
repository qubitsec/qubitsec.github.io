---
title: Log4Shell
permalink: ja_log4shell.html
sidebar: Video_HD_testing_ja
topnav: topnav_ja
---

<!-- <style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/9YtI-plPXm8' frameborder='0' allowfullscreen></iframe></div> -->

<br />

## 1. Log4Shellとは?

Log4Shell または CVE-2021-44228は、著名なjavaロギングフレームワーク Log4j のゼロデイ任意コード実行の脆弱性です。

この脆弱性はアリババのクラウドセキュリティチームによって2021年11月24日にアパッチに非公開で伝えられ、2021年12月9日に一般公開されました。

この脆弱性は、LDAPとJNDI要求を検査しないLog4jの特徴を利用して、攻撃者が任意のJavaコードをサーバーまたはその他のコンピュータで実行できるようにします。

Log4jプロジェクトを担当するアパッチソフトウェア財団は、Log4ShellにCVSS点数の最高点である10点を付与しました。

<br />

## 2. 模擬攻撃シナリオ

  1) 脆弱なLog4Shellを使用するVictimウェブサービスにアクセスしてpayloadを転送

  2) /etc/passwd 情報奪取
  
  3) 攻撃ログがPLURAで正常に収集されたか確認
  
  4) PLURAウェブファイアウォール(WAF) - Log4Shell攻撃に対するブロック試演

<br />

## 3. 参考サイト

  [1] Log4shell [http://blog.plura.io/?p=17912](http://blog.plura.io/?p=17912){: target="_blank"}

  [2] CVE-2021-44228 (Log4Shell) Apache Log4j セキュリティホール対応 : [http://blog.plura.io/?p=16659](http://blog.plura.io/?p=16659){: target="_blank"}

  [3] Apache Log4j 脆弱性 (CVE-2021-44228) アップデート案内 : [http://blog.plura.io/?p=16723](http://blog.plura.io/?p=16723){: target="_blank"}

