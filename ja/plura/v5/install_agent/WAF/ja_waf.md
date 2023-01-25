---
title: WAF Agent
permalink: ja_waf.html
sidebar: Install_A_W_ja
topnav: topnav_ja
---
     
     PLURA WAFは知られていない(Unknown)攻撃に対応するための機能を提供します。

     - 全ログ + 詳細な検出履歴提供 
     - リクエスト本文と応答値分析でクレデンシャルスタッフィング攻撃に対応 
     - 応答本文分析でデータ유출攻撃に対応 
     - SQLインジェクション正常に遮断対応 

<br />

## 1. 事前作業

PLURAウェブファイアウォールはAmazon Linux 2 AMI(又はCentOS 7)にインストール出来ます。

  - 1.1 ウェブファイアウォールをインストールするEC2インスタンスのターミナルに接続してroot権限でインストール
  - 1.2 タイムゾーン設定及び時刻同期化をシステムに合わせて設定

     `# timedatectl set-timezone Asia/Seoul`

     `# ntpdate time.google.com`

  - 1.3 ファイアウォール及びネットワークセキュリティ設定 

     - 80, 443などのウェブサービスに使用されるポートの接続を허용

<br />

## 2. インストール作業

  - 2.1 SWインストールコマンド

     `# curl https://repo.plura.io/v5/agent/install.sh | bash`

     `# /etc/plura/plura.sh install_waf`

  - 2.2 ヘルスチェッカーアップロード例外設定コマンド

     `# echo '[{"User-Agent": "ELB-HealthChecker/2.0"}]' > /etc/plura/conf/weblog-excluder.json`

  - 2.3 エージェント登録コマンド

     `# /etc/plura/plura.sh register [クライアント登録キー]`


