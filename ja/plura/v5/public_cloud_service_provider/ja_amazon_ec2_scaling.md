---
title: EC2 Auto Scaling 環境支援
permalink: ja_amazon_ec2_scaling.html
sidebar: PCSP_ja
topnav: topnav_ja
---

## 1. Amazon EC2 Auto Scaling とは?  
[https://docs.aws.amazon.com/ja_kr/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html](https://docs.aws.amazon.com/ja_kr/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html){:target="_blank"}

<br />

## 2. Amazon EC2 Auto Scaling 環境の構成例

[![image](/docs/images/Public_Cloud/ec2_autoscaling/01.png)](/docs/images/Public_Cloud/ec2_autoscaling/01.png){: target="_blank"}  
画像引用 : https://docs.aws.amazon.com

上記のような環境で、それぞれのインスタンスにPLURAエージェントをインストールして使用できます。
インスタンスがグループから分離されたりStandby状態になってもシステムが終了するのではなく、AutoScalingグループに接続された弾力的なロードバランサーからそのインスタンスが削除され、トラフィックがロードバランサーからこれらのインスタンスにルートされないだけなので、PLURAエージェントは引き続きログを収集します。

<br />

## 3. PLURAエージェント設定

PLURAエージェントで次のようにAutoScalingで活用する機能を設定することができます。

     [root@localhost]# vi /etc/plura/conf/plura.conf

     1. システム起動時のエージェントログイン遅延設定
     login_delay_sec = 0 (秒)

     2. AWS環境でAuto Scalingを使用する場合、インスタンス固有の識別子をPLURA V5システムに転送する設定(値が1のときに転送)
     login_with_machine_id = 0

     3. 複数のネットワークインターフェイスを使用する場合、PLURA V5ウェブに表示されるIPアドレス設定 
     interface = eth1 (システム > システム管理リストに表示される代表IP アドレスを指定)  
     interface_mon = eth1 (システム > リソース監視 > ネットワークトラフィックを収集するインターフェース設定)
      
     4. システム起動時のhostname変更によるログイン遅延設定
     login_hostname_check=0 (default = 0)  
     0 > 指定された遅延時間まで無条件に待つ  
     1 > hostname 変更が1回感知されると遅延中断。
     2 > hostname 変更が2回感知されると遅延中断。