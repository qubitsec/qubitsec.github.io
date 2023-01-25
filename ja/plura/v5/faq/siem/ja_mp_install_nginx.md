---
title: Nginx手動インストール
permalink: ja_mp_install_nginx.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

## 1. 事前調査

### 1-1. nginx実行可否検査

`# ps -ef|grep nginx`

     nginx 実行ファイルパス/ コマンドパラメータ確認(=readlink /proc/$(pid)/exe)

     nginx 設定ファイルパス確認(nginx -t)

     nginx process owner確認

<br />

### 1-2. サービス登録確認

`# service nginx status`

<br />

### 1-3. 再設定テスト

`# service nginx reload`

`# nginx -s`

<br />

### 1-4. 設定ファイル確認

     /etc/nginx/nginx.conf
     http {
     include conf.d/*.conf
     …

     → include conf.d/*.confラインがない場合は追加 !!!
     (nginx設定ファイルパス)/conf.d ディレクトリがない場合は生成!!!

<br />

## 2. 標準インストール

`# curl https://repo.plura.io/v4/module/nginx/plura.conf -o /etc/nginx/conf.d/plura.conf`

     → http {} ブロックにaccess_log指示語ラインが追加されウェブログが生成されます。

<br />

## 3. カスタマイズインストール

⭐注意 : server {}ブラックにaccess_log指示語がある場合, 親ブロックhttp {} ブロックのaccess_log
指示語が無視されます。よって下記の通り, 手動でaccess_log指示語ラインを追加する必要があります。

     server {
     access_log /var/log/plura/weblog.log mod_plura;

<br />

## 4. 情報登録

`# echo ModPlura-Nginx > /etc/modplura`

`# echo 5.5.0 >> /etc/modplura`

`# echo /usr/sbin/nginx >> /etc/modplura`

`# echo /etc/nginx >> /etc/modplura`

`# touch /etc/.modplura`

<br />

## 5. 権限イシュー

⭐注意 : PLURAウェブログ生成ディレクトリのownerをnginx worker processのownerで変更します。

`# chown nginx /var/log/plura`