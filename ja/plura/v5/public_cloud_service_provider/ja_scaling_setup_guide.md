---
title: Auto Scaling 設定ガイド
permalink: ja_scaling_setup_guide.html
sidebar: PCSP_ja
topnav: topnav_ja
---


## PLURAのAmazon EC2 Auto Scaling 環境支援

[https://qubitsec.github.io/ja_amazon_ec2_scaling.html](https://qubitsec.github.io/ja_amazon_ec2_scaling.html){:target="_blank"}

PLURA V5エージェントがインストールされたインスタンスをAutoScalingする際に考慮すべき事項があります。

PLURA V5はIPアドレスとホスト名を基準にエージェントを識別し、新規IPアドレスを持つ新しいAuto Scalingインスタンスが生成されるとPLURA V5エージェントが自動的に追加/登録されます。 インスタンスが終了しても、登録済みエージェントは自動削除されず、エージェントの状態だけが [停止] ステータスに変更されます。

したがって、インスタンスが終了してから再び生成される時、既存に使用していたIPアドレスではなく、別のIPアドレスを割り当てられると、管理されるPLURA V5エージェントの数が増え続けます。

新規インスタンスが作成されるときに、限られた数量サイズのプールからIPアドレスを割り当てられるようにすると、管理されるエージェント リストのサイズが不要に増加しないように制限できます。

パブリックIPアドレスをあらかじめ確保しておいて使用しない場合、不要な費用が発生するので、ここでは内部IPアドレスを割り当てる方法を例に説明します。

> 1.  固定IPアドレス確保
> 2.  エージェントのインストール
> 3.  Auto Scalingイメージ作成
> 4.  スタートテンプレートの作成
> 5.  Auto Scaling グループ作成
> 6.  インスタンス作成/終了テスト

<br />

### 1. 固定IPアドレスの確保

-   新規インスタンスに割り当てる固定IPアドレスサブネットの確保

    自動生成される流動IPアドレスと衝突しないように固定IPアドレス専用サブネットを確保します。

    (インスタンスが複数の可用領域で生成される場合、各可用領域ごとにサブネットを作成します。)  

    <!-- [![image](/docs/images/Public_Cloud/autoscaling_setup/01.png)](/docs/images/Public_Cloud/autoscaling_setup/01.png){: target="_blank"}-->

<br />

-   固定IPを指定したネットワークインターフェイスの作成

    Auto Scaling 最大容量だけネットワークインターフェースをあらかじめ生成し、それぞれに固定IPアドレスをあらかじめ割り当てます。

    後でこのIPアドレスリストをuser-dataに入力することになります。

    <!-- [![image](/docs/images/Public_Cloud/autoscaling_setup/02.png)](/docs/images/Public_Cloud/autoscaling_setup/02.png){: target="_blank"}-->

    Description項目に"plura-waf"文字列入力→user-dataスクリプトで識別子として使用する）

<br />

### 2. エージェントのインストール

-   PLURA V5エージェントのインストール後、次の設定ファイルに内容を追加します。  
    vi /etc/plura/conf/plura.conf
    
    > interface=eth1  
    > login_delay_sec=60
    

<br />

### 3. Auto Scaling イメージ作成

-   エージェントがインストールされているインスタンスの画像を作成します。

    <!-- [![image](/docs/images/Public_Cloud/autoscaling_setup/03.png)](/docs/images/Public_Cloud/autoscaling_setup/03.png){: target="_blank"}-->

    <!-- [![image](/docs/images/Public_Cloud/autoscaling_setup/04.png)](/docs/images/Public_Cloud/autoscaling_setup/04.png){: target="_blank"}-->

<br />

### 4.スタートテンプレートの作成

-   Auto Scaling グループで使用する開始テンプレートを作成します。

    <!-- [![image](/docs/images/Public_Cloud/autoscaling_setup/05.png)](/docs/images/Public_Cloud/autoscaling_setup/05.png){: target="_blank"}-->

<br />

-   スタートテンプレートコンテンツ項目で、前段階で作成したAMI画像を指定します。

    <!-- [![image](/docs/images/Public_Cloud/autoscaling_setup/06.png)](/docs/images/Public_Cloud/autoscaling_setup/06.png){: target="_blank"}-->

<br />

-   고高度な詳細 > ユーザー データ項目に固定IP アドレスとホスト名割り当てスクリプトを入力します。

    <!-- [![image](/docs/images/Public_Cloud/autoscaling_setup/07.png)](/docs/images/Public_Cloud/autoscaling_setup/07.png){: target="_blank"}-->

<br />

-   固定IP アドレスおよびホスト名割り当てスクリプトについては、以下を参照してください。

    (環境に合わせてアクセスキー、秘密キー、IPアドレスの値を修正します。)  

    <!-- [![image](/docs/images/Public_Cloud/autoscaling_setup/08.png)](/docs/images/Public_Cloud/autoscaling_setup/08.png){: target="_blank"}-->

<br />

### 5. AutoScalingグループの作成

-   Auto Scaling グループを作成し、前の段階で作成した開始テンプレートを指定します。

    <!-- [![image](/docs/images/Public_Cloud/autoscaling_setup/09.png)](/docs/images/Public_Cloud/autoscaling_setup/09.png){: target="_blank"}-->

    <!-- [![image](/docs/images/Public_Cloud/autoscaling_setup/10.png)](/docs/images/Public_Cloud/autoscaling_setup/10.png){: target="_blank"}-->

<br />

### 6. インスタンス作成/終了テスト

-    Auto Scaling グループ > 詳細 情報 タブ > グループ 詳細 [編集] 押して グループ サイズ 調整

    <!-- [![image](/docs/images/Public_Cloud/autoscaling_setup/11.png)](/docs/images/Public_Cloud/autoscaling_setup/11.png){: target="_blank"}-->

<br />

-   目的の容量項目に値を指定して、手動でインスタンスの数を変更できます。

    <!-- [![image](/docs/images/Public_Cloud/autoscaling_setup/12.png)](/docs/images/Public_Cloud/autoscaling_setup/12.png){: target="_blank"}-->

<br />

-   PLURA V5 ページのシステム > システム管理でエージェントのリストを確認

    <!-- [![image](/docs/images/Public_Cloud/autoscaling_setup/13.png)](/docs/images/Public_Cloud/autoscaling_setup/13.png){: target="_blank"}-->

<br />
    
-   新しいIPアドレスおよびホスト名で新しいインスタンスが作成されると、エージェントが自動的に追加されます。

    その後、インスタンスが終了してもエージェントは削除されず、動作状態だけが [中止] に変更されます。

    (アイコンの状態が変更されるまで最大5分かかります。)  

    <!-- [![image](/docs/images/Public_Cloud/autoscaling_setup/14.png)](/docs/images/Public_Cloud/autoscaling_setup/14.png){: target="_blank"}-->

<br />

-   新しく生成されたインスタンスが既に登録されたエージェントのIPアドレス/ホスト名と同じであれば、システム管理画面にエージェントが新たに追加される代わりにステータスだけが変更されます。
 
    (アイコンの状態を直ちに変更태 즉시 변경)