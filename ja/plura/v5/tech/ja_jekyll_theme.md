---
 title: Theme apply
 permalink: ja_jekyll_theme.html
 sidebar: Tech_ja
 topnav: topnav_ja
---
## 1. テーマ選択

[jamstackthemes.dev](https://jamstackthemes.dev/ssg/jekyll/)

[jekyllthemes.org](http://jekyllthemes.org/)

[jekyllthemes.io](https://jekyllthemes.io/)

[jekyll-themes.com](https://jekyll-themes.com/)

<br />

## 2. テーマ適用

### 1) 選択したテーマ Git Repository 移動
- Repositoryを download zip

<br />

### 2) ダウンロードしたフォルダを開く
- ダウンロードしたフォルダの圧縮解除
- ファイル全体のコピー

<br />

### 3) username.github.ioに貼り付ける
- 完全コピーしたファイルを貼り付ける
- 同じ名前のファイルは上書き

<br />

### 4) bundle コマンド実行
- cmd または vsc terminalで username.github.io パスに移動して以下のコマンドを実行

<code>bundle install</code>

<code>bundle exec jekyll serve</code>

<br />

### 5) ローカルサーバー接続
- 127.0.0.1:4000にアクセスすると、適用されたテーマページに表示
- 確認後、pushまたは変更してpushして保存