---
 title: Make Jekyll Blog
 permalink: ja_make_b.html
 sidebar: Tech_ja
 topnav: topnav_ja
---



## 1. VSCode

[VSCode ダウンロード](https://code.visualstudio.com/download){:target="_blank"}
をします。

<br />

## 2. Git


[Git 新規登録](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home){:target="_blank"}
を行います。

新しいRepositoryを作成します。

Repositoryの名前は ex) username.github.io

リモート接続をするためにAdd a README fileをチェックする必要があります。

<br />

[https://git-scm.com](https://git-scm.com/){:target="_blank"}
 に接続して、自分のオペレーティング システムに合ったバージョンのGitをインストールします。

[![image](/docs/images/Tech/Jekyll_Blog/Blog_1.PNG){: width="" }](/docs/images/Tech/Jekyll_Blog/Blog_1.PNG){: target="_blank"}

[![image](/docs/images/Tech/Jekyll_Blog/Blog_2.PNG){: width="" }](/docs/images/Tech/Jekyll_Blog/Blog_2.PNG){: target="_blank"}

[![image](/docs/images/Tech/Jekyll_Blog/Blog_3.PNG){: width="" }](/docs/images/Tech/Jekyll_Blog/Blog_3.PNG){: target="_blank"}

**上記の画像3つを除き、残りは基本設定**

<br />

## 3. Ruby
[Rubyダウンロード](https://www.ruby-lang.org/ja/){:target="_blank"}


[![image](/docs/images/Tech/Jekyll_Blog/ja_Blog_4.PNG){: width="" }](/docs/images/Tech/Jekyll_Blog/ja_Blog_4.PNG){: target="_blank"}


すべて進行するとcmdウィンドウが表示されますが、3番を選択してください。

<br />

## 4. Git連動 cmd or VSC(terminal)

 git config –global user.name [github アカウント]

 git config –global user.email [github e-mail]

 <br />

 デスクトップにフォルダを作成または保存したいパスに作成します。

 作成したフォルダへ移動 / cdコマンドで移動
 git clone (git repository HTTPSアドレス を貼り付け)
   - 成功したら You appear to have cloned an empty repository メッセージが表示
   - 作成したフォルダの中に、フォルダがもう1つ作成されています。

<br />

### 4-1. Git アップロード(適用)

**1. cmd**
   - git add [filename]
   - git commit -m “name(スナップショットの概念なので、自分がやりたい名前に設定します。)”
   - git push // gitにアップしたいファイルが載っています。

**2. vsc**

   - ctrl + s (保存) = ターミナルに完了表示が出たら、まずローカル環境で確認できます。
   - 虫眼鏡アイコンクリック
   - 入れるタイトル入力
   - ctrl + enter
   - sync ~~ クリック

<br />

## 5. Jekyll Install
cmd 実行

gem install jekyll

bundle install


cd C:\(~~~)
   - ご自身のブログフォルダに移動


jekyll new .

bundle exec jekyll serve
   - cmdにローカルアドレス表示(仮想環境開始)
   
   ex) 127.0.0.1~~~
