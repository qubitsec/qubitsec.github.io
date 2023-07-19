---
title: データ流出
permalink: ja_data_exfiltration_solution.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

データ流出検出例外事項とソルーションに対して説明します。

<br />

## 1. Content-Type : MIMEタイプ検査 

※ MIMEタイプとは, クライアントに転送されたドキュメントの多様性を知らせるメカニズムです。

### 1.1. 動作出来るタイプ

PLURA V5では下記のタイプに限って動作します。

  **text**

     テキストを含めてる全ての文書を指し、議論上人が読めることでなければなりません。
     例) text/plain, text/html, text/css, text/javascript

<br />

  **マルチタイプ**

     マルチパートタイプは一般的に他のMIMEタイプを持つ個別なパートで分かれるドキュメントのカテゴリーを指します。 

 <br />

## 2. Content-Encoding

 PLURA V5では圧縮解凍(Disable Compression)問題で例外処理(検査しません。)

<br />

## 3. charset=UTF-8

※ <meta> タグのcharset属性は該当HTMLドキュメントの文字エンコード方式を明示します。

 PLURA V5はUTF-8に限って動作します。<font color='dodgerblue'> (Windows-IISの場合) </font>

<br />

### 3-1. 案内フレーズ

応答本文を選択した場合、、表示される案内プレート 

 フィルタ検出は出来されたが応答本文を読めない場合、下のプレートが表示されます。

<!-- [![image](/docs/images/Additianal/data/1.png)](/docs/images/Additianal/data/1.png){: target="_blank"}-->

<br />

### 3-2. 問題点

 応答本文文字エンコーディングがUTF-8ではない, ハングルのようにマルチバイト(multi-byte)エンコーディングになっている場合発生します。

<br />

### 3-3. ソルーション

 応答本文がUTF-8で応答出来るようにウェブドキュメントに下のコマンドを入れてください。


**<meta charset=”UTF-8″>**

[![image](/docs/images/Additianal/data/ja_2.png)](/docs/images/Additianal/data/ja_2.png){: target="_blank"}

<br />

 ウェブドキュメントを保存する時、エンコーディングをUTF-8にしてください。

[![image](/docs/images/Additianal/data/ja_3.png)](/docs/images/Additianal/data/ja_3.png){: target="_blank"}

<br />

## 4. MIMEタイプ整理

MIMEタイプは個別タイプとマルチタイプで分けられます。

 **個別タイプ**
      text/plain
      text/html
      image/jpeg
      image/png
      audio/mpeg
      audio/ogg
      audio/*
      video/mp4
      application/octet-stream
      …

 個別タイプはドキュメントのカテゴリーを指し、下記の一つになれます。 

[![image](/docs/images/Additianal/data/ja_4.png){: width="800" }](/docs/images/Additianal/dataja_4.png){: target="_blank"}

<br />

     特定サーブタイプがないテキストドキュメントにはtext/plainが使用される必要があります。
     特定あるいはサーブタイプが既知のサーブタイプがないバイナリドキュメントについては, application/octet-streamが使用される必要があります。

<br />

**マルチパートタイプ**

     multipart/form-data
     multipart/byteranges

     マルチパートタイプは一般的に他のMIMEタイプを持つ個別パートに分かれるドキュメントのカテゴリーを指します。
     つまり, このタイプは合成ドキュメントを表す方法です。
     HTML FormsとPOSTメソッドの関係で使用されるmultipart/form-data, そして全体ドキュメントのサブセットのみを転送するための206 Partial Content状態メッセージと共に使用されるmultipart/byterangesを除いて, HTTPがマルチパートドキュメントを処理できる特定方法は存在しません。: メッセージはブラウザで簡単に転送されます。(ドキュメントをインラインへどのように表示かわからないので, ‘名付けて保存’ ウィンドウを表示します。)

<br />

参考サイト

 1. Content-Type : MIMEタイプ検査[https://mzl.la/327am7k](https://mzl.la/327am7k){: target="_blank"}

 2. Content-Encoding [https://bit.ly/31ecOJW](https://bit.ly/31ecOJW){: target="_blank"}

 3. charset=UTF-8 [https://theqoop.tistory.com/266](https://theqoop.tistory.com/266){: target="_blank"}

 4. ApacheサーバーでHTTP圧縮非活性化[https://qubitsec.github.io/ja_apache_http_compression.html](https://qubitsec.github.io/ja_apache_http_compression.html){: target="_blank"}