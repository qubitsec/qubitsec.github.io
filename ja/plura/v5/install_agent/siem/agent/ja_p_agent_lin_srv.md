---
title: Linux Server
permalink: ja_p_agent_lin_srv.html
sidebar: Install_A_S_ja
topnav: topnav_ja
---



     以下はCentOS 7バージョンのインストールプロセスの例です。
     必ずwww.plura.ioの右上のInstall Agentsページから確認の後、インストールしてください。

<br />

## Linux Server Agentインストールし<!-- 映像 -->

<!-- <style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/TW7_NF1gF9g' frameborder='0' allowfullscreen></iframe></div> -->

<br />

## 1. PLURA V5 Agentインストール

`# sudo -s`

`# curl https://repo.plura.io/v5/agent/install.sh | bash`

<br />

## 2.ライセンス登録及び実行

`# /etc/plura/plura.sh register ****`

<br />

## 3.インストール情報確認

`# /etc/plura/pluraagent -version`

Version: x.x.x

<br />

__PLURA V5 Agent Linux Srvインストール<!-- 映像 -->__

– Linux Syslogインストール<!-- 映像 --> : [https://qubitsec.github.io/ja_lin_sys.html](https://qubitsec.github.io/ja_lin_sys.html){:target="_blank"}

– Linux Syslog-Auditインストール<!-- 映像 --> : [https://qubitsec.github.io/ja_linu_sys_audit.html](https://qubitsec.github.io/ja_linu_sys_audit.html){:target="_blank"}

– Linux Apache / Nginxインストール<!-- 映像 --> : [https://qubitsec.github.io/ja_lin_apache_nginx.html](https://qubitsec.github.io/ja_lin_apache_nginx.html){:target="_blank"}

– Linux Web Server – Datosインストール<!-- 映像 --> : [https://qubitsec.github.io/ja_lin_web_server.html](https://qubitsec.github.io/ja_lin_web_server.html){:target="_blank"}

<br />

## 4. ファイル追加

追加設定が必要な場合、下記の順番でファイルを追加します。

インストールパスが選択出来ます。

`# vi /etc/plura/conf/plura.conf`

     # システム起動時、エージェントログイン遅延の設定
     login_delay_sec = 0 (秒)

     # AWS環境でAuto Scalingを使用する時インスタンス固有識別子をPLURA V5システムに転送する設定(値が1の時転送)
     login_with_machine_id = 0

     # 複数のネットワークインターフェイスを使用する時PLURA V5ウェブに表示されるIPアドレス設定
       interface = eth1 (システム > システム管理リストに出るマスターアドレスを設定)
       interface_mon = eth1 (システム > リソースモニタリング > ネットワークトラフィックを収集するインターフェイス設定)


     # システム起動時のhostname変更によるログイン遅延の設定
       login_hostname_check=0 (default = 0)
     # 0 > 設定された遅延時間まで無期限待機。
     # 1 > hostname変更が1回検出されたら遅延中断
     # 2 > hostname変更が2回検出されたら遅延中断

<br />

## 5. CentOS 6 End of Lifetime (EOL)対応

エージェントインストール前に下記のコマンドを実行


`# mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.org`

     * CentOS Product Specifications
       https://wiki.centos.org/About/Product

       メーカーがサポートを終了した製品についてPLURAV5でもサポートを終了します。
       PLURAV5でサポートされていないオペレーティングシステムバージョンを使用すると、問題が発生する可能性があります。
       メーカーがサポートを終了したバージョンを使用している場合は、アップグレードについてより積極的な検討が必要です。 ハッキングや障害など、さまざまな問題に直面し、深刻な問題に発展する可能性があるからです。
      
      
      
      
