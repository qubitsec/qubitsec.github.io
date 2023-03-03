---
 title: Make Jekyll Blog
 permalink: ja_make_b.html
 sidebar: Tech_ja
 topnav: topnav_ja
---



## [vscode]

[vscode ダウンロード](https://code.visualstudio.com/download)します。

<br />

## [Git]


[Git サインイン](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)を行います。

新しい Repository 作成

Repository 名前は ex) username.github.io

Add a README file をチェックします。 // 理由は remote をするためです。

<br />

[git-scm.com](git-scm.com) に接続して Git をインストール (右下のモニター図に自分のオペレーティングシステムに合うバージョンがわかります。)

<!-- [![image](/docs/images/Tech/Jekyll_Blog/Blog_1.PNG){: width="600" }](/docs/images/Tech/Jekyll_Blog/Blog_1.png){: target="_blank"}-->

<!-- [![image](/docs/images/Tech/Jekyll_Blog/Blog_2.PNG){: width="600" }](/docs/images/Tech/Jekyll_Blog/Blog_2.png){: target="_blank"}-->

<!-- [![image](/docs/images/Tech/Jekyll_Blog/Blog_3.PNG){: width="600" }](/docs/images/Tech/Jekyll_Blog/Blog_3.png){: target="_blank"}-->

**上記の画像3つを除き、残りは基本設定**

<br />

## [Ruby]
[https://www.ruby-lang.org/ko/](Ruby ダウンロード)

<!-- [![image](/docs/images/Tech/Jekyll_Blog/Blog_4.PNG){: width="600" }](/docs/images/Tech/Jekyll_Blog/Blog_4.png){: target="_blank"}-->

最新バージョンをダウンロードします。

すべて進むとするとcmdウィンドウが出てくるが、3回押します。
<br />

## [Git 連動] cmd or VSC(terminal)

 git config –global user.name [github アカウント]

 git config –global user.email [github e-mail]

 <br />

 デスクトップフォルダの作成or保存したいパス

 作成したフォルダに移動/cdコマンドに移動
 git clone (git repository HTTPS アドレス貼り付け)
   - 成功すれば You appear to have cloned an empty repository とメッセージが出ます。
   - 作成したフォルダに行くとフォルダがもう一つ作成されている。

<br />

### Git アップロード(適用)

**1. cmd**
   - git add [filename]
   - git commit -m “name(スナップショットの概念なので、ご自身がやりたい名前に設定。)”
   - git push // gitに載せたいファイルが載っております。

**2. vsc**

   - ctrl + s (保存) = ターミナルに完了表示が出れば、まずローカル環境で確認できる。
   - 拡大鏡アイコンをクリック
   - 入れる名前を入力
   - ctrl + enter
   - sync ~~ クリック

<br />

## [Jekyll Install]
cmd 実行

gem install jekyll

bundle install


cd C:\(~~~)
   - ご自身のブログフォルダへ移動


jekyll new .

bundle exec jekyll serve
   - cmdにローカルパスが表示されます。(仮想環境がスタート)
   
   ex) 127.0.0.1~~~
