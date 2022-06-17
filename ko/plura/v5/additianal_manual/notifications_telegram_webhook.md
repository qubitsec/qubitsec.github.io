---
title: Webhook 설정으로 Telegram에서 PLURA V5 알림 받아보기
permalink: notifications_telegram_webhook.html
sidebar: Add_M
topnav: topnav
---

텔레그램 메신저를 이용해 웹훅 수신을 설정하면 PLURA V5 탐지 알림을 텔레그램으로 받아볼 수 있습니다.

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/lIFuWAtDVbk' frameborder='0' allowfullscreen></iframe></div>


#### 1. Bot 생성

     BotFather 검색
     /newbot 입력
     Bot 이름 등록
     Bot 식별키 등록(_bot으로 끝나야함)
     Bot 생성 이후 출력창의 t.me/Bot식별키를 클릭하여 시작(start)을 눌러서 활성화

#### 2. Bot 을 그룹채팅에 초대

     그룹을 만들고 생성한 Bot 이름으로 검색하여 등록
     Bot생성시 Token을 이용해서 현재 그룹채팅의 id 정보를 확인
     https://api.telegram.org/bot{Token}/getUpdates

#### 3. 확인한 정보를 PLURA V5 알림설정에 등록

     예) https://api.telegram.org/bot{Token}/sendmessage?parse_mode=Markdown&chat_id={id}