---
title: オンラインPoC進行方法案内
permalink: ja_cl_secaas_poc.html
sidebar: faq_common_M_ja
topnav: topnav_ja
---


     PLURA V5を使用するための案内です。
     会員登録 > ログイン > EDRエージェントのインストールで行われ、3分以内に完了します。

<br />


## 1. PLURA PoC 進行概要

<br />

(1) 会員登録によるアカウント作成    
(2) ログイン後、顧客サポート要請申請    
(3) エージェントインストール (Install Agents)

<br />

### 1-1. PLURA アカウント作成

- 無料トライアル開始 
   - [https://www.plura.io/signup/](https://www.plura.io/signup/){: target="_blank"}

<!--
[![image](/docs/images/Additianal/cloud/1.png){: width="800" }](/docs/images/Additianal/cloud/1.png){: target="_blank"}
-->

- E-mail承認 > 登録済み（無料トライアルライセンス14日）
- 要求時に試用版ライセンス延長を提供

<br />

### 1-2. カスタマーサポートリクエスト

- ログ分析支援のためにアカウント作成完了後、次のように「カスタマーサポートリクエスト」を選択
   - 要請事由の作成　例）ハッキング攻撃探知及び対応
   - メニュー位置:左上メニューPLURA V5ロゴの右を確認 > 管理 > サービス > カスタマーサポートリクエスト
   [https://qubitsec.github.io/ja_manage_service.html](https://qubitsec.github.io/ja_manage_service.html){: target="_blank"}

[![image](/docs/images/Additianal/cloud/ja_2.png){: width="800" }](/docs/images/Additianal/cloud/ja_2.png){: target="_blank"}

<br />

### 1-3. 同僚招待(オプション)
※ 追加の管理者が必要な場合は、同僚を招待できます。
- ログインアカウントに同僚招待
- 分析対象システムへの統合管理の提供
- メニュー位置:左上 > 管理 > メンバー > メンバー追加
[https://qubitsec.github.io/ja_manage_member.html](https://qubitsec.github.io/ja_manage_member.html){: target="_blank"}

<br />

## 2. エージェントのインストール

### 2-1. ログイン後エージェントのインストール “Install Agents”

- Install Agentsページ案内またはエージェントインストール映像を参考にしてエージェントインストール

<!--
- 윈도우 서버에 에이전트 설치 예시   
[https://qubitsec.github.io/ja_p_agent_win_srv.html](https://qubitsec.github.io/ja_p_agent_win_srv.html){: target="_blank"}
-->

- Windows エージェントのインストールの例   
[https://qubitsec.github.io/ja_p_agent_edr_win.html](https://qubitsec.github.io/ja_p_agent_edr_win.html){: target="_blank"}

<br />

### 2-2. 事前環境確認
- 「Install Agents」でシステム環境に合う文書が見つからない場合は、対象サーバーのOSバージョン、ウェブサーバーの種類とバージョン、ウェブサービスポート情報を確認する   
- 該当内訳に従って正確なインストールページをご案内いたします。

<br />

### 2-3. エージェントのインストール - 遠隔サポート

- 必要な事前情報  

  - 対象サーバーの接続情報(Windowsユーザー権限、Linux root権限)
  - 対象サーバーのOSバージョン、ウェブサーバーの種類とバージョン、ウェブサービスポート情報(例:CentOS 8 / Apache 2.4 / TCP 80)
  -  Windowsの場合、Sysmonをインストールしてこそ、より正確で十分な異常兆候検出が可能です。
Sysmon インストールガイド : [https://qubitsec.github.io/ja_sysmon.html](https://qubitsec.github.io/ja_sysmon.html){: target="_blank"}

<br />
 
## 3. PLURA V5 マニュアル
- [https://qubitsec.github.io/](https://qubitsec.github.io/){: target="_blank"}
