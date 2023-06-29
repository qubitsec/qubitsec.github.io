---
 title: Theme apply
 permalink: ja_jekyll_theme.html
 sidebar: Tech_ja
 topnav: topnav_ja
---

## 1. テーマ選択

[jamstackthemes.dev](https://jamstackthemes.dev/ssg/jekyll/){:target="_blank"}

[jekyllthemes.org](http://jekyllthemes.org/){:target="_blank"}

[jekyllthemes.io](https://jekyllthemes.io/){:target="_blank"}

[jekyll-themes.com](https://jekyll-themes.com/){:target="_blank"}

<br />

## 2. テーマ適用

### 2-1. 選択したテーマ Git Repository 移動
- リポジトリを download zip

<br />

### 2-2. ダウンロードしたフォルダを開く
- ダウンロードしたフォルダの圧縮解凍
- ファイル全体をコピー

<br />

### 2-3. username.github.ioに貼り付ける
- 全体コピーしたファイルを貼り付ける
- 同じ名前のファイルは上書き

<br />

### 2-4. bundle コマンド実行
- cmd または vsc terminal から username.github.io 経路を移動して下記のコマンドを実行

<code>bundle install</code>

<code>bundle exec jekyll serve</code>

<br />

### 2-5. ローカルサーバ接続
- 127.0.0.1:4000にアクセスすると、適用されたテーマページが表示
- 確認後 push 又は変更して push し、保存