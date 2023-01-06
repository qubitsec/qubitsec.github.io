---
title: Linux Syslog-Audit
permalink: ja_lin_sys_audit.html
sidebar: Install_A_S
product: Install_A_S
---

## Linux Agent Audit Logアクティブ映像

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/8WYGIsW08yY' frameborder='0' allowfullscreen></iframe></div>

<br />

## 1. Syslog Auditアクティブ

- 下記の1-1, 1-2番中選択

<br />

### 1-1. Audit Logパッケージ個別インストール

- CentOS, Red Hat, Amazon Linux   
`# yum -y install audit audisp-plugins`

- Ubuntu   
`# apt -y update`   
`# apt -y install auditd audispd-plugins`

<br />

ユーザーインターフェースに応じて下記のパッケージをインストールしてください。

- CentOS, Red Hat, Amazon Linux   
`# yum -y install cronie logrotate rsyslog`

- Ubuntu   
`# apt -y update`   
`# apt -y install cron logrotate rsyslog`

<br />

### 1-2. Syslog+Auditログパッケージ総合インストール

- PLURA V5 Agent事前インストール要
- 総合インストール
`# /etc/plura/plura.sh install_syslog`

<br />

## 2. Auditログ確認

アクティブ状態のAuditログ次のメニューで確認出来ます。

- フィルター検出 > システム > チャンネル"Auditlog"選択
- 全ログ > システム > チャンネル"Auditlog"選択
