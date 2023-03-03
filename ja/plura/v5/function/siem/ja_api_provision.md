---
title: API 提供(On-premise 専用)
permalink: ja_api_provision.html
sidebar: M_SIEM_ja
topnav: topnav_ja
---

     提供するAPIに加工することで、必要な情報を得ることができます。
     On-premise環境でのみご利用いただけます。

## 1. API認証キー設定
- グループ管理 > 連動設定メニューから設定できます。
- 発行ボタンを押すと、次のようにAPI認証キーが発行されます。
<!-- [![image](/docs/images/Manual/siem/api/1.png)](/docs/images/Manual/siem/api/1.png){: target="_blank"}-->
 

## 2. 提供される情報
- 発行された認証キーを使用して、Rest API方式で照会作業を行うことができます。
- ログの情報は提供していません。
- 次の情報が提供されます。

      - 検出ログ件数:相関分析、システムログ、ウェブログ、ネットワークログ、アカウント奪取攻撃
      - 全体ログ件数:オペレーティングシステム、サーバIPアドレス、ホスト名、発生時間
      - サーバ別の全体ログおよび検出対象件数
      - コンプライアンスメニュー別検知件数
      - 全体ログ、検知ログチケット発行件数
      - ログ流入量(時/日/週/月)
      - エージェントインストールサーバ数及び全体ログ及びウェブログ収集可否、システムログ収集可否
      - サーバ別情報（エージェント正常動作状態、登録情報など）
      - WebファイアウォールブロックIPの大量登録
      - 検知ログ危険度基準検知数提供