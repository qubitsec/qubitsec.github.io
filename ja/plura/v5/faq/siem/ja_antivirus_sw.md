---
title: ワクチンソフトウェア終了検出方法
permalink: ja_antivirus_sw.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

## 1. Windows Defender終了検出

**フィルタ名“Windows Defender終了”でデフォルト提供。**
 
<br />

## 2. 他のワクチンソフトウェア終了検出

**ウェブからフィルタ登録することで設定方法**

2-1. フィルタ > 登録 > システム選択

<br />

2-2. サーバグループ選択 > オペレーティングシステムWindows選択 > Securityチャンネル選択 > 詳細追跡分類選択 > イベントタイプ選択


<!-- [![image](/docs/images/Additianal/anti/1.png){: width="800" }](/docs/images/Additianal/anti/1.png){: target="_blank"}-->
 
<br />

イベントタイプでプロセス終了(4689)選択

<!-- [![image](/docs/images/Additianal/anti/2.png)](/docs/images/Additianal/anti/2.png){: target="_blank"}-->

絵のように選択後、‘データ値’に使用するワクチンの必修プロセス名を入れて下段の‘登録’ボタンをクリック

<br />

**例Alyac**
<!-- [![image](/docs/images/Additianal/anti/3.png){: width="800" }](/docs/images/Additianal/anti/3.png){: target="_blank"}-->

<br />

`# C:\Program Files\ESTsoft\ALYac\AYRTSrv.aye`

<br />

**例V3**
<!-- [![image](/docs/images/Additianal/anti/4.png){: width="800" }](/docs/images/Additianal/anti/4.png){: target="_blank"}-->

<br />

`# C:\Program Files\AhnLab\V3*\ASDSvc.exe`

<br />

**예시 Kaspersky**

<!-- [![image](/docs/images/Additianal/anti/5.png)](/docs/images/Additianal/anti/5.png){: target="_blank"}-->

<br />

`# C:\Program Files*\Kaspersky Lab\*\avp.exe`

<br />

**例Symantec Norton**

<!-- [![image](/docs/images/Additianal/anti/6.png){: width="800" }](/docs/images/Additianal/anti/6.png){: target="_blank"}-->

<br />

`# C:\Program Files\Norton Security\Engine\*\NortonSecurity.exe`