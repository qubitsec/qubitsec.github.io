---
title: Windows
permalink: ja_p_agent_edr_win.html
sidebar: Install_A_E_ja
product: Install_A_E_ja
---

<br />

MS Windows用EDR Agentのインストール方法をご案内します。

      EDR用 Windows Agentで、Windows ServerとDesktop (PC) の両方に対応します。
      マイターアタック(MITRE ATT&CK)ベースのAPTハッキング攻撃に対応します。
      ユーザー行為ログを分析し、異常行為検出時の攻撃を検知またはブロックします。

## インストール案内

<!-- 샘플 : __1.1 파일 다운로드__ -->

### 1. EDR エージェントをダウンロード

下記からEDRエージェントのインストールファイルをダウンロード

[ダウンロード](https://repo.plura.io/v4/agent/win/PluraSetup.exe)

<br />

### 2. EDR エージェントのインストール開始

インストール対応言語を選択してください。

[![image](/docs/images/ja/Install_Agents/EDR/Agent/install1.PNG)](/docs/images/ja/Install_Agents/EDR/Agent/install1.PNG){:target="_blank"}

<br />

### 3. インストールパス選択

デフォルトのパスに加えて、ユーザーはインストールパスを修正できます。

<br />

[![image](/docs/images/ja/Install_Agents/EDR/Agent/install2.PNG)](/docs/images/ja/Install_Agents/EDR/Agent/install2.PNG){:target="_blank"}

<br />

### 4. ログイン

(1) インストールが完了すると、ログインウィンドウが自動的に実行されます。

(2) ウェブページで確認したライセンスを入力します。
- ライセンス確認場所 : PLURAウェブログイン後、上段 > 管理 > ライセンスです。

[![image](/docs/images/ja/Install_Agents/EDR/Agent/install3.PNG)](/docs/images/ja/Install_Agents/EDR/Agent/install3.PNG){:target="_blank"}

<br />

### 5. サービススタート

(1) ログインすると、EDRエージェントは自動的に開始されます。

(2) 最後のログアップロード時間が表示されたら、ログが正常にアップロードされていることになります。

[![image](/docs/images/ja/Install_Agents/EDR/Agent/install4.PNG)](/docs/images/ja/Install_Agents/EDR/Agent/install4.PNG){:target="_blank"}

<br />

### 6. Sysmon インストール

* Sysmon エージェントは MS Windows Internalが提供しているソフトウェアです。
* Windowsシステムの行為を理解するために、できればインストールをお勧めします。

<br />

(1) Sysmon ダウンロード

最新バージョンのダウンロードリンク : [ Sysmon ](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon){:target="_blank"}

<br />

(2) インストール

* 管理者権限でcmd実行してSysmon.exeファイルのパスに移動

* 下記のコマンド実行
`sysmon.exe -accepteula -i “C:\Program Files\PLURA\sysmon-plura.xml”`

<br />

(3) 確認

* EDR Agentで Sysmonインストール確認

[![image](/docs/images/ja/Install_Agents/EDR/Agent/install5.PNG)](/docs/images/ja/Install_Agents/EDR/Agent/install5.PNG){:target="_blank"}

<br />

### 7. サービス中止

アクティブな 'エージェント ステータス' ボタンを選択すると、EDR エージェントサービスが停止されます。

<!-- [![image](/docs/images/Ins_G/Agent_W/Agent_W_5.png)](/docs/images/Ins_G/Agent_W/Agent_W_5.png){:target="_blank"} -->

[![image](/docs/images/ja/Install_Agents/EDR/Agent/install6.PNG)](/docs/images/ja/Install_Agents/EDR/Agent/install6.PNG){:target="_blank"}

<br />

### 8. ウェブログ収集設定

* ウェブログを収集する機能を追加する内容です。

<br />

(1) <font color='dodgerblue'> https://plura.io </font> に接続して、該当するシステムのウェブログ収集機能を有効にします。

* 左メニューの下部に、システム > システム管理

* リストの中から変更したい項目を選択

(2-1) ウェブログ収集ON後、修正ボタンの選択、解除をご希望の場合はOFFにします。

[![image](/docs/images/ja/Install_Agents/EDR/Agent/install7.PNG)](/docs/images/ja/Install_Agents/EDR/Agent/install7.PNG){:target="_blank"}

<br />

(2-2) または、エージェントのウェブログ設定メニューからウェブログ収集チェックをします。 解除をご希望の場合は、OFFしてください。

[![image](/docs/images/ja/Install_Agents/EDR/Agent/install8.PNG)](/docs/images/ja/Install_Agents/EDR/Agent/install8.PNG){:target="_blank"}

<br />

<!--
## Step 3

__자동 업데이트 기능__

PLURA V5 Agent 자동 업데이트 기능을 사용하시려면 환경설정 탭으로 이동하여 자동업데이트 체크박스에 체크 되어있는지 확인합니다. 기본값은 체크 상태입니다.

[![image](/docs/images/Ins_G/Ins_EDR/002.png)](/docs/images/Ins_G/Ins_EDR/002.png){:target="_blank"}

<br>



## Step 4

__업데이트 확인__

PLURA V5 Agent의 업데이트 버전은 C:\Program Files\PLURA 경로에서 확인 하실 수 있습니다.

**ex)PLURAService 버전 확인**

[![image](/docs/images/Ins_G/Ins_EDR/003.png){: width="800" }](/docs/images/Ins_G/Ins_EDR/003.png){:target="_blank"}

<br>

[![image](/docs/images/Ins_G/Ins_EDR/004.png)](/docs/images/Ins_G/Ins_EDR/004.png){:target="_blank"}

<br>

-->


<!-- 주석 Sample
-->



<!--
######### 삭제된 내용
## Windows Agent 설치 영상

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/kKLL_sP9w9c' frameborder='0' allowfullscreen></iframe></div>

## 웹로그 수집 설정 영상
<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/kKLL_sP9w9c' frameborder='0' allowfullscreen></iframe></div>
-->

