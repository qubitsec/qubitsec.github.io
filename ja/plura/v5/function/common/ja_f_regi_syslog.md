---
title: Syslog
permalink: ja_f_regi_syslog.html
sidebar: M_C_ja
topnav: topnav_ja
---

## 1. Syslog フィルタ登録
- ボタンをクリックして、登録するログの詳細を入力します。
- 適用された推奨フィルタの内容を参照してください。

     1-1. フィルタ分類: フィルタの分類を選択します。  
     1-2. グループ: フィルタに使用するシステムグループを選択します。 
     1-3. オペレーティングシステムグループ: オペレーティング システムの種類を選択します。
     1-4. チャンネル: OS別にチャンネルを選択してフィルタを登録することができます。
     1-5. フィルタ名: 簡単に識別できる名前で決めます。  
     1-6. フィルタの危険度: フィルタの危険度を設定できます。  
     1-7. フィルタ状態: 設定したフィルタで検出したログをフィルタ検知メニューから表示するかどうかを設定できます。  
     1-8. 情報入力   
    - 1-8-1. 要素の選択: リストされているデータ名を選択します。
    - 1-8-2. データ値: フィルタリングを必要とする値を入力します。
    - 1-8-3. 含む/除外: フィルタリング時に入力値を含む/除外して通知を受け取ります。

 <br />

以下は登録例です。

<!-- [![image](/docs/images/Manual/common/filter2/syslog/1.png){: width="800" }](/docs/images/Manual/common/filter2/syslog/1.png){: target="_blank"}-->  

<br />

## 2. フィルタ検出条件の例

**2-1.** 以下のように2つ以上のデータグループがあるとき、グループ同士はAND条件です。

<!-- [![image](/docs/images/Manual/common/filter2/syslog/2.png){: width="800" }](/docs/images/Manual/common/filter2/syslog/2.png){: target="_blank"}-->  

<br />

<!-- [![image](/docs/images/Manual/common/filter2/syslog/3.png){: width="800" }](/docs/images/Manual/common/filter2/syslog/3.png){: target="_blank"}-->  

<br />

**2-2.** 以下のように1つのグループに複数のデータ値があるとき、グループ内の値同士はOR条件です
<!-- [![image](/docs/images/Manual/common/filter2/syslog/4.png){: width="800" }](/docs/images/Manual/common/filter2/syslog/4.png){: target="_blank"}-->  


ユーザー定義フィルタ登録 DEMO : [https://qubitsec.github.io/ja_system_weblog.html](https://qubitsec.github.io/ja_system_weblog.html){: target="_blank"} 