---
title: Credential Stuffing
permalink: ja_credential_stuffing.html
sidebar: Video_HD_testing_ja
topnav: topnav_ja
---

<!-- <style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/_LA7p-IeOOY' frameborder='0' allowfullscreen></iframe></div> -->

<br />

## 1. クレデンシャルスタッフィング(Credential stuffing) 攻撃とは?

クレデンシャルスタッフィング(Credential stuffing)は、インターネットユーザが同じログイン情報(IDとパスワード)を複数のウェブサイトやサービスで使用することに対する攻撃方法です。

クレデンシャルスタッフィング攻撃はハッカーが一般的に公開された、または流出した認証情報(ログイン情報)リストを使用して大量にログインしようとすることです。

この時、ほとんどのサイトがログイン試行回数制限機能を持っているため、攻撃者は複数のサーバーとIPアドレスを使用して大規模なログインを試みることができます。

<br />

## 2. 模擬攻撃シナリオ

  1) 模擬攻撃により一定時間継続的にページアクセスを試みる(※模擬攻撃使用ツール:Apache Jmeter)

  2) 攻撃ウェブログがPLURAで正常に収集されたか確認
  
  3) PLURAアカウント乗っ取りフィルタにより、クレデンシャルスタッフィング(Credential stuffing)攻撃検知確認

<br />

## 3. 참고사이트

  [1] 管理 > セキュリティ設定 [https://qubitsec.github.io/ja_manage_security.html](https://qubitsec.github.io/ja_manage_security.html){: target="_blank"}

  [2] ML検知 [https://qubitsec.github.io/ja_ml.html](https://qubitsec.github.io/ja_ml.html){: target="_blank"}

  [3] Webファイアウォール > 防御設定 [https://qubitsec.github.io/ja_defense_setting_waf.html](https://qubitsec.github.io/ja_defense_setting_waf.html){: target="_blank"}

  [4] クレデンシャルスタッフィング攻撃に対応する [http://blog.plura.io/?p=18955](http://blog.plura.io/?p=18955){: target="_blank"}

  [5] ウェブサービス攻撃に対応する [http://blog.plura.io/?p=18875](http://blog.plura.io/?p=18875){: target="_blank"}


