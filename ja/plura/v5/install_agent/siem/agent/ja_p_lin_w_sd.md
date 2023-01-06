---
title: Linux Web Server-Datos
permalink: ja_p_lin_w_sd.html
sidebar: Install_A_S
product: Install_A_S
---


     Datosはウェブトラフィックをモニタリングするためのツールです。
     モニタリングにはネットワークインターフェイスのポット情報のみを使用するため、他プロセスとの競合を発生しません。

<br />

次のような環境で使用出来ます。

1) ウェブサーバーにApache HTTPD, Nginxではない環境、例えば,Apache Tomcatの単独使用の場合

2) コンテナ環境で、ホストに複数のウェブPOD使用する場合

<br />

## Linux Web Server – Datosインストール映像

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/TqDUR002tt0' frameborder='0' allowfullscreen></iframe></div>

<br />

__[Datos]マルチポットロギング__


Datosは一つのエージェントから一つのIP:PORTデータのみロギング出来ます。
複数のIPアドレス及びPORTデータをロギングするなら必要な数だけDatosサービスを生成する必要があります。

Datosサービスを追加生成する方法は下記のようです。

<br />

## 1. Datos設定ファイル追加

`# vi /etc/datos/conf/httplogger2.conf`

     interface=eth1
     logfile=/var/log/plura/weblog2.log

     host=172.16.10.52

     port=8080

<br />

## 2. Datosサービスファイル追加
`# vi /etc/datos/conf/datos2.service`

     [Unit]
     Description=Datos httplogger service

     After=network.target

     [Service]

     Type=simple

     User=root

     WorkingDirectory=/etc/datos/

     ExecStart=/etc/datos/httplogger -name datos2 /etc/datos/conf/httplogger2.conf

     ExecStop=/etc/datos/httplogger -name datos2 -stop

     Restart=always

     [Install]

     WantedBy=multi-user.target

<br />

## 3. Datosサービス追加登録

`# cp /etc/datos/conf/datos2.service /usr/lib/systemd/system/datos2.service`

`# systemctl enable datos2.service`

<br />

## 4. Datosサービス追加実行
     
`# service datos2 start`

<br />

## 5. システム > システム管理メニューにファイル登録

設定 > ウェブログ収集パスに事前に設定した　__/var/log/plura/weblog2.log__ パス追加

[![image](/docs/images/Ins_G/Linux_WebServer_Datos/webserver_datos.png)](/docs/images/Ins_G/Linux_WebServer_Datos/webserver_datos.png){:target="_blank"}