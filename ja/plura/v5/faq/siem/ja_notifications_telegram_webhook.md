---
title: Webhook設定でTelegramから受け取る
permalink: ja_notifications_telegram_webhook.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

     テレグラムメッセンジャーを使用してウェブフックの受信を設定するとPLURA V5検出通知をテレグラムで確認出来ます。 

<br />

## 1. グループ通知(ウェブフック設定)映像

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/lIFuWAtDVbk' frameborder='0' allowfullscreen></iframe></div>

<br />

## 2. テレグラムでウェブフック設定

### 2-1. Bot生成

     BotFather検索
     /newbot入力
     Bot名登録
     Bot識別キー登録(_botで終わらせる必要があります。)
     Bot生成後、出力ウィンドウのt.me/Bot識別キーのスタート(start)をクリックして活性化

<br />

### 2-2. Botをグループチャットに招待

     グループを生成し、Bot名で検索して登録
     Bot生成する時、 Tokenを使用して現在グループチャットのidを確認
     https://api.telegram.org/bot{Token}/getUpdates

<br />

### 2-3. 通知設定

確認した情報をPLURA V5通知設定に登録

     例) https://api.telegram.org/bot{Token}/sendmessage?parse_mode=Markdown&chat_id={id}