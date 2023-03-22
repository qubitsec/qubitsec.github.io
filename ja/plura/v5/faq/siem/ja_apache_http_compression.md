---
title: ApacheサーバーでHTTP圧縮非活性化
permalink: ja_apache_http_compression.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

     ウェブサーバーでHTTP圧縮を非活性化して動作するとPLURA V5からデータ流出行為を検出出来ます。
     次はApacheサーバーでHTTPが圧縮されているか確認して圧縮を非活性化する方法です。

<br />

## 1. HTTP圧縮のためサーバーテスト

 ヘッダーに下記の通り要請を追加してHTTP圧縮を確認します。

     Accept-Encoding:compress,gzip

 圧縮が活性化されているとサーバーは圧縮されているページを応答し, 圧縮をサポートしない場合は一般テキストに応答します。

 <br />

## 2. CentOS/Red HatでHTTP圧縮非活性化

`# sudo vi /etc/httpd/conf/httpd.conf`

     #LoadModule deflate_module modules/mod_deflate.so
     (この行を注釈処理)

`# service httpd restart`

<br />

## 3. UbuntuでHTTP圧縮非活性化

`# sudo a2dismod deflate`

`# sudo /etc/init.d/apache2 restart`

<br />

参考資料  
[データ流出検出例外事項とソルーション](https://qubitsec.github.io/ja_data_exfiltration_solution.html){: target="_blank"}