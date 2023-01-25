---
title: 再送信攻撃の使い方案内
permalink: ja_hack_re_attack.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

### 1. PLURA V5 Manual – 再送信攻撃映像

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/_ICFu8Rg5h0' frameborder='0' allowfullscreen></iframe></div>

<br />

**再送信攻撃**とは, 検出ログを使用して実際に攻撃を確認する機能で模擬ハッキングの一環です。

**再送信攻撃**で模擬ハッキングをする理由は攻撃の成功と失敗を確認するためです。
SQLインジェクション攻撃の成功は非常に深刻な危険にさらされるので成功に対して必ず確認する必要がありますが
多数の攻撃ログの中で模擬ハッキングをテストすることは簡単ではありません。

PLURAの再送信攻撃はこのような不便をなくし、業務効率を最大化するため提供しています。

“**再送信攻撃**”ボタンは再転送攻撃の条件成立のみ表示されるので常に見えない可能性があります。

また, ユーザーブラウザで進行されるので該当ホスト(Host), URLに接近出来るネットワーク環境でなければ正常に動作しない可能性があります。
つまり、 ネットワークの影響を受けます。

<br />

### 2. HTTP Method 再転送対象

2-1. GET全ログ

2-2.
POST | PUT | PATCH | DELETEの場合はパラメータ名が存在し,Content-typeも存在するログ

<br />

### 3. Content-Type 再転送対象

3-1. application/x-www-form-urlencoded : key/value形式

3-2. application/json : json形式

3-3. application/xml :xml形式

下のイメージはMethod – GET方式(application/x-www-form-urlencoded)の攻撃で再転送攻撃条件が成立し、再送信攻撃ボタンが表示されることを確認出来ます。

 [![image](/docs/images/Additianal/hack/1.png){: width="800" }](/docs/images/Additianal/aws/1.png){: target="_blank"}

<br />

編集ボタンをクリックしてプロトコル&ポートを変更出来ます。(デフォルトはhttps : 443)

httpsを使用しない場合、http : 80で修正して再送信攻撃データを転送出来ます。
修正された値は保存されます。

 [![image](/docs/images/Additianal/hack/2.png)](/docs/images/Additianal/aws/2.png){: target="_blank"}
 
 <br />

**“curl://” ボタン** 選択する時、自動コピー(再転送Queryが生成)されウェブ転送方式よりもっと多様な攻撃オプションを提供します。

※ **“curl://” 攻撃オプション:** 再転送攻撃 + 全Method含め(GET, POST, PUT, PATCH, DELETE, HEAD, OPTION, CONNECT, TRACE)

<br />

### 4. HTTP Method再転送対象ではない場合 – 再送信攻撃ボタン非表示

4-1. POST (上段再転送可能条件が未成立の場合)

4-2. PUT (上段再転送可能条件が未成立の場合)

4-3. PATCH (上段再転送可能条件が未成立の場合)

4-4. DELETE (上段再転送可能条件が未成立の場合)

4-5. HEAD

4-6. OPTION

4-7. CONNECT

4-8. TRACE

<br />

### 5. Content-Types再転送対象ではない場合 – 再送信攻撃ボタン非表示

5-1. multipart/form-data : key/value 形式 (バイナリ含め)

5-2. application/octet-stream : バイナリファイル

5-3. text/yaml : yml
