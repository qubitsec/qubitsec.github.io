---
title: Windowsエージェントのインストール権限
permalink: ja_window_agent_install_authority.html
sidebar: faq_common_M_ja
topnav: topnav_ja
---

<br />

## Administratorグループに属するユーザーアカウント(管理者アカウント)

     Administratorグループに属するユーザーアカウント(管理者アカウント)でPLURA V5インストール後、 
     ログオフ又はシステムリブートする時、スタートアッププログラムに登録されたTrayプログラムがUACの影響で 
     実行出来ない可能性があります。
     一方、ウィンドウサービスに登録されたPLURAService.exeはsystem権限で実行されるので 
     影響を受けずに正常に実行出来ます。

<br />

## Administratorアカウント

     AdministratorアカウントはUAC(User Account Control,ユーザーアカウントコントロール)の影響を受けないが、他の全ユーザー 
     (Administratorsグループに属するユーザー含めて)は影響を受けます。
     よってPLURA V5プログラムインストールはAdministratorアカウントでインストールしたらシステムの再起動 
     又はログオフ後、にもスタートメニューに登録されたPLURATray.exeが正常に動作します。
     System権限で動作するPLURAService.exeは影響がありません。