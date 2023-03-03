---
title: Syslog設定でkiwiから受け取る
permalink: ja_send_syslog_kiwi.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

<br />

## 1. Kiwiダウンロード及びインストール

 ダウンロードURL: [https://www.kiwisyslog.com/free-tools/kiwi-free-syslog-server](https://www.kiwisyslog.com/free-tools/kiwi-free-syslog-server){: target="_blank"}

 <!-- [![image](/docs/images/Faq/kiwi/05.png){: width="800" }](/docs/images/Faq/kiwi/05.png){: target="_blank"}-->

<br /> 

## 2. Kiwi Syslog実行

インストールしたKiwi Syslogを実行すると, 下のような画面が出ます。

 <!-- [![image](/docs/images/Faq/kiwi/01.png){: width="800" }](/docs/images/Faq/kiwi/01.png){: target="_blank"}-->

<br />

## 3. ショートカット実行

プログラム上段"File" → "Setup"又は"Ctrl+P" ショートカットを実行します。

 <!-- [![image](/docs/images/Faq/kiwi/02.png){: width="800" }](/docs/images/Faq/kiwi/02.png){: target="_blank"}-->

<br />

## 4. Source IP Address追加

Inputsオプション → Source IP Addressを追加します。

 <!-- [![image](/docs/images/Faq/kiwi/03.png){: width="800" }](/docs/images/Faq/kiwi/03.png){: target="_blank"}-->

<br />

## 5. 設定追加

### 5-1. [送信] PLURA設定

PLURAページ左上の管理 > 連動メニューから下記のように設定出来ます。

[グループ通知-syslog連動設定](https://qubitsec.github.io/ja_manage_peristalsis.html#4-syslog-%EC%97%B0%EB%8F%99-%EC%84%A4%EC%A0%95){: target="_blank"}

  - 受信先IPアドレスを入力
 
 <br />
 
### 5-2. [受信] Kiwi Syslog設定

  - Kiwi Memu > File > Setup > Inputs > UDP > Data encoding : UTF-8 設定
  - Kiwi Memu > File > Setup > Inputs > IP addressesメニューに下の送信先のIPアドレスを全てAdd
     - 211.43.190.184
     - 211.43.190.185
     - 211.43.190.186
     - 211.43.190.187
     - オンプレミス環境の場合、送信先のIPアドレスは上のIPアドレスと違います。
 






 