---
title: MySQL Error & Slow-Query ログ
permalink: ja_mysql_err_slow_query_log.html
sidebar: Install_A_S_ja
topnav: topnav_ja
---


     アプリケーション : MySQL ErrorログとSlow-Queryログの取り込みための設定

<br />

## 1. アプリケーションログ収集設定

### 1-1. 設定パス

システム  > システム管理 > サーバ選択 > 設定メニュー > 設定ボタンをクリックします。

<!-- [![image](/docs/images/Ins_G/mysql_slow/1.png){: width="800" }](/docs/images/Ins_G/mysql_slow/1.png){:target="_blank"} -->

<br />

### 1-2. アプリケーション原本ログ収集設定アクティブ

<!-- [![image](/docs/images/Ins_G/mysql_slow/2.png){: width="800" }](/docs/images/Ins_G/mysql_slow/2.png){:target="_blank"} -->

<br />

### 1-3. パス > 設定ボタンをクリック

<!-- [![image](/docs/images/Ins_G/mysql_slow/3.png){: width="800" }](/docs/images/Ins_G/mysql_slow/3.png){:target="_blank"} -->

<br />

### 1-4. タグ選択及びパス入力
MySQL ErrorログとSlow-Queryログのパスを入力します。

<!-- [![image](/docs/images/Ins_G/mysql_slow/4.png)](/docs/images/Ins_G/mysql_slow/4.png){:target="_blank"} -->

<br />

### 1-5. 入力情報確認

タグが正常に登録されたことを確認後、修正ボタンをクリックします。

<!-- [![image](/docs/images/Ins_G/mysql_slow/5.png)](/docs/images/Ins_G/mysql_slow/5.png){:target="_blank"} -->

<br />

<!-- [![image](/docs/images/Ins_G/mysql_slow/6.png){: width="800" }](/docs/images/Ins_G/mysql_slow/6.png){:target="_blank"} -->

<br />

- タグ登録方法
   - アプリケーションログ収集設定のためのタグが登録出来ます。
   - パス : 管理 > リスト > アプリケーションタグ 

<br />

- 設定ボタンをクリックします。

<!-- [![image](/docs/images/Ins_G/mysql_slow/7.png){: width="800" }](/docs/images/Ins_G/mysql_slow/7.png){:target="_blank"} -->

<br />

- 登録ボタンをクリックして、登録しようとするタグを入力します。

<!-- [![image](/docs/images/Ins_G/mysql_slow/8.png){: width="800" }](/docs/images/Ins_G/mysql_slow/8.png){:target="_blank"} -->

<br />

## 2. MySQL – SLOW QUERY設定

### 2.1. 設定

`# vi /etc/my.cnf`

[mysqld]

slow_query_log = 1

slow_query_log_file = /var/log/mysql-slow.log

long_query_time = 3

<br />

### 2.2. ログファイル生成及び権限設定

`# touch /var/log/mysql-slow.log`

`# chown mysql.mysql /var/log/mysql-slow.log`

<br />

### 2.3. 権限確認

`# ls -aZ /var/log/mysql*`

<!-- [![image](/docs/images/Ins_G/mysql_slow/9.png)](/docs/images/Ins_G/mysql_slow/9.png){:target="_blank"} -->

### 2.4. mysql restart

`# systemctl restart mysqld`

<br />

### 2.5. アクティブ確認
`mysql> show variables like ‘slow_query_%’;`

<!-- [![image](/docs/images/Ins_G/mysql_slow/10.png)](/docs/images/Ins_G/mysql_slow/10.png){:target="_blank"} -->

<br />

## 3. ログ確認

Mysql Error及びSlow Queryログ発生後、アプリケーションログでMySQLのログを確認します。
登録したタグ名で検索できます。

<br />

内部ブログ

[アプリケーションログログアップロード設定](https://qubitsec.github.io/ja_set_app_log_up.html){:target="_blank"}