---
title: Windows Server
permalink: ja_p_agent_win_srv.html
sidebar: Install_A_S_ja
topnav: topnav_ja
---





## Windows Server Agentインストール映像

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/kKLL_sP9w9c' frameborder='0' allowfullscreen></iframe></div>

<br />

インスタンス方法です。手順に進んでください。


      メーカーがサポートを終了した製品についてPLURAV5でもサポートを終了します。
      PLURAV5でサポートされていないオペレーティングシステムバージョンを使用すると、問題が発生する可能性があります。
      メーカーがサポートを終了したバージョンを使用している場合は、アップグレードについてより積極的な検討が必要です。
      ハッキングや障害など、さまざまな問題に直面し、深刻な問題に発展する可能性があるからです。
      

## Step 1

PLURA V5 AgentはMicrosoft .NET Framework 3.5以上がインスタンスされていると使用出来ます。
Windows Server 2012からデフォルトで設置されています。

<br />

## Step 2

まず、当システムから<font color='dodgerblue'> www.plura.io </font>ログイン後、右上の <font color='dodgerblue'> Install Agents </font> をクリックしてダウンロードします。

__2.1 インストール.__

Administratorアカウントでインストールする必要があります。

[![image](/docs/images/Ins_G/Agent_W/Agent_W_1.png)](/docs/images/Ins_G/Agent_W/Agent_W_1.png){:target="_blank"}

インストールパスを選べます。

[![image](/docs/images/Ins_G/Agent_W/Agent_W_2.png)](/docs/images/Ins_G/Agent_W/Agent_W_2.png){:target="_blank"}

<br />

__2.2 ログイン__

(1) インストールが完了するとログインウィンドウが自動的に起動されます。

(2) ウェブページから確認したライセンスを入力します。

[![image](/docs/images/Ins_G/Agent_W/Agent_W_3.png)](/docs/images/Ins_G/Agent_W/Agent_W_3.png){:target="_blank"}

<br />

__2.3 サービス開始__

(1) ログインするとPLURA V5 Log-Fのサービスが開始されます。

(2) 最後のログアップロード時間が確認出来た場合ログが正常にアップロードされている状態です。

[![image](/docs/images/Ins_G/Agent_W/Agent_W_4.png)](/docs/images/Ins_G/Agent_W/Agent_W_4.png){:target="_blank"}

<br />

__2.4 サービス中止__

(1) アクティブされている‘エージェント状態’ボタンをクリックするとPLURA V5サービスが中止されます。

[![image](/docs/images/Ins_G/Agent_W/Agent_W_5.png)](/docs/images/Ins_G/Agent_W/Agent_W_5.png){:target="_blank"}

[![image](/docs/images/Ins_G/Agent_W/Agent_W_6.png)](/docs/images/Ins_G/Agent_W/Agent_W_6.png){:target="_blank"}

<br />

## Step 3
__3.1 IISサーバウェブロク使用方法__

Step 2までは‘システムログ’収集に対する内容で、Step 3は‘ウェブサーバログ’を収集する機能を追加する内容です。
‘システムログ’だけ必要するならこのStepはスキップしてください。
ウェブログ取り込は下記の順番に進んでください。

(1) <font color='dodgerblue'> www.plura.io </font>に接続して当システムのログ収集機能をアクティブさせます。

* システム > システム管理に入ります。

* システムリストの中、ユーザーのシステムIPアドレスに当たるリストをクリックします。

(2-1) ウェブログ収集をチェックにしてOKボタンをクリックします。解除する場合はチェックを外してください。

[![image](/docs/images/Ins_G/Agent_W/Agent_W_7.png){: width="800" }](/docs/images/Ins_G/Agent_W/Agent_W_7.png){:target="_blank"}

(2-2) 又はエージェントのウェブログ設定メニューでウェブログ収集をチェックします。解除する場合はチェックを外してください。

[![image](/docs/images/Ins_G/Agent_W/Agent_W_8.png)](/docs/images/Ins_G/Agent_W/Agent_W_8.png){:target="_blank"}

<br />

(3) しばらく待つと __[Visual C++再頒布可能パッケージ]__　インストールアラームが出ます。

[OK]をクリックし、下からの2番目の画像のように再頒布可能パッケージをインストールすると、ウェブログ取り込み機能を正常に使用出来ます。

[![image](/docs/images/Ins_G/Agent_W/Agent_W_9.png)](/docs/images/Ins_G/Agent_W/Agent_W_9.png){:target="_blank"}

手動ダウンロードリンク : [Visual Studio 2012 Visual C++再頒布可能パッケージ](https://download.microsoft.com/download/1/6/B/16B06F60-3B20-4FF2-B699-5E9B7962F9AE/VSU_4/vcredist_x64.exe){:target="_blank"}

手動ダウンロードリンク : [Visual Studio 2013 Visual C++再頒布可能パッケージ](https://download.microsoft.com/download/2/E/6/2E61CFA4-993B-4DD4-91DA-3737CD5CD6E3/vcredist_x64.exe){:target="_blank"}

<br />

## Step 4

__4.1 自動アップデート機能__

環境設定メニューから自動アップデートのチェックボックスにチェックされているとPLURA V5 Agentの自動アップデート機能を使用出来ます。 デフォルトはチェック状態です。

[![image](/docs/images/Ins_G/Agent_W/Agent_W_10.png)](/docs/images/Ins_G/Agent_W/Agent_W_10.png){:target="_blank"}

<br />

## Step 5

__5.1 アップデート確認__

PLURA V5 AgentのアップデートバージョンはC:\Program Files (x86)\PLURAパスで確認出来ます。

**ex)PLURAServiceバージョン確認**

[![image](/docs/images/Ins_G/Agent_W/Agent_W_11.png){: width="800" }](/docs/images/Ins_G/Agent_W/Agent_W_11.png){:target="_blank"}

<br />

[![image](/docs/images/Ins_G/Agent_W/Agent_W_12.png)](/docs/images/Ins_G/Agent_W/Agent_W_12.png){:target="_blank"}

<br />

## ウェブログ収集設定映像
<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/kKLL_sP9w9c' frameborder='0' allowfullscreen></iframe></div>


