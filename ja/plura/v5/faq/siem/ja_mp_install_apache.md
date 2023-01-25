---
title: Apache 手動インストール
permalink: ja_mp_install_apache.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

## 1. 事前調査

`# ps -ef|grep httpd`

`# ps -ef|grep apache`

     → apache実行ファイルパス/ コマンドパラメータ確認(=readlink /proc/$(pid)/exe)
     apache process owner確認

`httpd|apache2 -V`
     → apache設定ファイルパス確認

`httpd|apache2 -v`
     → apacheバージョン確認

<br />

### 1-1. サービス登録確認

`# service httpd|apache2 status`

<br />

### 1-2. 再設定テスト

`# service httpd|apache2 reload`

`${apache2dir}/bin/apachectl graceful`

`${apache2dir}/bin/httpd -k graceful`

<br />

### 1-3. 設定ファイル確認

標準インストール = /etc/httpd/conf.d/

     /etc/httpd/conf/httpd.conf
     IncludeOptional conf.d/*.conf

<br />

カスタマイズインストール = /usr/local/apache2/conf/extra/

     /usr/local/apache2/conf/httpd.conf
     Include conf/extra/plura.conf
     → 最後のラインに追加!!!

<br />

## 2. 標準インストール

`# curl https://repo.plura.io/v4/module/apache/centos/plura.conf -o /etc/httpd/conf.d/plura.conf`

`# curl https://repo.plura.io/v4/module/apache/centos/x86_64/7/2.4/mod_plura_module.so -o /etc/httpd/modules/mod_plura_module.so`

<br />

## 3. カスタマイズインストール

`# curl https://repo.plura.io/v4/module/apache/centos/plura.conf -o /usr/local/apache2/conf/extra/plura.conf`

`# curl https://repo.plura.io/v4/module/apache/centos/x86_64/7/2.4/mod_plura_module.so -o /usr/local/apache2/modules/mod_plura_module.so`

<br />

plura.confファイル内容

     LoadModule mod_plura_module modules/mod_plura_module.so
     mp_log /var/log/plura/weblog.log

<br />

## 4. 情報登録

`# echo ModPlura-Apache > /etc/modplura`

`# echo 5.5.3 >> /etc/modplura`

`# echo /usr/sbin/httpd >> /etc/modplura`

`# echo /etc/httpd >> /etc/modplura`

`# echo /etc/httpd >> /etc/modplura`

`# echo centos/x86_64/7/2.4 >> /etc/modplura`

`# touch /etc/.modplura`

<br />

## 5. カスタマイズインストール

`# echo /usr/local/apache2/bin/httpd >> /etc/modplura`

`# echo /usr/local/apache2 >> /etc/modplura`

`# echo /usr/local/apache2 >> /etc/modplura`

<br />

## 6. 権限イシュー

⭐注意 : PLURAウェブログ生成ディレクトリのownerをapache worker processのownerで変更します。

`# chown apache /var/log/plura`

`# chmod 755 /var/log/plura`

`# chmod +x /etc/httpd/modules/mod_plura_module.so`

<br />

⭐selinux オブジェクトの設定

`# chcon -h system_u:object_r:httpd_sys_content_t:s0 /etc/httpd/conf.d/plura.conf`

`# chcon -h system_u:object_r:httpd_sys_content_t:s0 /etc/httpd/modules/mod_plura_module.so`

`# restorecon /etc/httpd/conf.d/plura.conf`

`# restorecon /etc/httpd/modules/mod_plura_module.so`