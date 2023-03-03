---
title: ウェブ
permalink: ja_f_web.html
sidebar: M_C_ja
topnav: topnav_ja
---

     リアルタイムでハッキングログを検知してリストを表示するページです。
     PLURA V5 Agentは、クライアントがサーバに要請したデータをメソッド別に分けてログを分析し、攻撃タイプ、攻撃コード、攻撃目的、脆弱項目などを示します。
     検知可能攻撃タイプはOWASP TOP 10です。 

<br />

ショートカット  [ウェブログの使用設定方法](https://qubitsec.github.io/ja_system_weblog.html){: target="_blank"}

<br />

## 1. 検出されたログの詳細
- 検出されたログリストをクリックすると、それぞれのログに含まれている詳細が表示されます。

<!-- [![image](/docs/images/Manual/common/filter/web/1.png){: width="800" }](/docs/images/Manual/common/filter/web/1.png){: target="_blank"}-->

<br />

 "再送信攻撃"ボタンは、再送信攻撃の条件が成立した場合にのみ表示されるため、常に見えない場合があります。

- 編集ボタンをクリックしてプロトコル&ポートを変更することができます。（基本設定はhttps:443）
- httpsを使用しない場合、http:80に修正して再送信攻撃データを送信することができます。 修正された値は保存されます。

<!-- [![image](/docs/images/Manual/common/filter/web/2.png)](/docs/images/Manual/common/filter/web/2.png){: target="_blank"}-->

<br />

- “curl://” ボタンを選択すると、自動コピー（再送信Queryが生成）され、ウェブ転送方式よりも多くの攻撃オプションを提供します。
※ “curl://” 攻撃オプション:再送信攻撃+すべてのMethodを含む(GET, POST, PUT, PATCH, DELETE, HEAD, OPTION, CONNECT, TRACE)

<br />

## 2. 検出されたログソースの内容
- <ログ詳細> ボタンをクリックすると、発生した原本の内容を確認できます。

<!-- [![image](/docs/images/Manual/common/filter/web/3.png){: width="800" }](/docs/images/Manual/common/filter/web/3.png){: target="_blank"}-->

<br />

## 3. コンプライアンス[label](https://gw.namutech.co.kr/gw/userMain.do)
- ‘コンプライアンス’ ボタンをクリックすると、発生したログにマッチングされるコンプライアンス項目を確認できます。

<!-- [![image](/docs/images/Manual/common/filter/web/4.png){: width="800" }](/docs/images/Manual/common/filter/web/4.png){: target="_blank"}-->


<br />

**データ流出** : データ流出が発生した場合、漏えい情報項目に表示されます。

<!-- [![image](/docs/images/Manual/common/filter/web/5.png){: width="800" }](/docs/images/Manual/common/filter/web/5.png){: target="_blank"}-->

<font color='dodgerblue'> ※ データ流出情報がある場合は、以下のように漏えい情報TABが追加され、その内容を確認することができます。 </font>

<br />

## 4. データ流出情報の確認
- 検出されたログリストをクリック > 流出情報 Tab > 検出されたログの流出情報の詳細を見ることができます。

<!-- [![image](/docs/images/Manual/common/filter/web/6.png){: width="800" }](/docs/images/Manual/common/filter/web/6.png){: target="_blank"}-->

<br />

- 検出されたログリストをクリック > 流出情報 Tab > 応答本文流出領域を表示ボタンをクリック
- 漏えいした応答本文の内容を確認できます。

<!-- [![image](/docs/images/Manual/common/filter/web/7.png){: width="800" }](/docs/images/Manual/common/filter/web/7.png){: target="_blank"}-->

<br />

## 5. 全体ログリンク
- ログ検出履歴でマウスの右ボタンをクリックすると、時間帯別のログページに移動できます。
- 全体ログ(=) : 検出されたフィルタ検出履歴 **“同じ時間帯”** に全体ログページに移動
- 全体ログ(±1s) : 検出されたフィルタ検出履歴 **“1초”** 前後の時間帯に全体ログページに移動
- 全体ログ(±5s) : 検出されたフィルタ検出履歴 **“5초”** 前後の時間帯に全体ログページに移動
- 全体ログ(±60s) : 検出されたフィルタ検出履歴 **“60초”** 前後の時間帯に全体ログページに移動

<!-- [![image](/docs/images/Manual/common/filter/web/8.png){: width="800" }](/docs/images/Manual/common/filter/web/8.png){: target="_blank"}-->

<br />

## 6. 項目別整列
- 日付/リクエストサイズ/応答サイズ/同一ログを基準に並べ替えることができます。

<!-- [![image](/docs/images/Manual/common/filter/web/9.png){: width="800" }](/docs/images/Manual/common/filter/web/9.png){: target="_blank"}-->
 
<br />

## 7. ページあたりのログ数
- 1 ページあたりの見えるログの数を 20 個、30 個、40 個、50 個に設定できます。

<!-- [![image](/docs/images/Manual/common/filter/web/10.png){: width="800" }](/docs/images/Manual/common/filter/web/10.png){: target="_blank"}-->

<br />

## 8. 日付/時間選択
- 過去の日付と時刻を選択してログを表示できます。

 <!-- [![image](/docs/images/Manual/common/filter/web/11.png){: width="800" }](/docs/images/Manual/common/filter/web/11.png){: target="_blank"}-->

<br />

## 9. グループ選択
- ユーザーが登録したシステム グループを選択して表示できます。

<!-- [![image](/docs/images/Manual/common/filter/web/12.png){: width="800" }](/docs/images/Manual/common/filter/web/12.png){: target="_blank"}-->

<br />

## 10. オペレーティングシステムの選択
- オペレーティング システムを選択して表示できます。

<!-- [![image](/docs/images/Manual/common/filter/web/13.png){: width="800" }](/docs/images/Manual/common/filter/web/13.png){: target="_blank"}-->

<br />

## 11. システムIPアドレス選択
- 希望するシステムIPアドレスを選択して見ることができます。

<!-- [![image](/docs/images/Manual/common/filter/web/14.png){: width="800" }](/docs/images/Manual/common/filter/web/14.png){: target="_blank"}-->
 
<br />

## 12. 分類選択
- 分類別に選択して見ることができます。

<!-- [![image](/docs/images/Manual/common/filter/web/15.png){: width="800" }](/docs/images/Manual/common/filter/web/15.png){: target="_blank"}-->
 
<br />

## 13. コード選択
- OWASP TOP10に選定された脆弱性別に選択して見ることができます。

<!-- [![image](/docs/images/Manual/common/filter/web/16.png){: width="800" }](/docs/images/Manual/common/filter/web/16.png){: target="_blank"}-->
 
<br />

## 14. 危険度選択
- 危険度を選択して見ることができます。

<!-- [![image](/docs/images/Manual/common/filter/web/17.png){: width="800" }](/docs/images/Manual/common/filter/web/17.png){: target="_blank"}-->
 
<br />

## 15. ステータス値選択
- ステータス値を選択して表示できます。


 <!-- [![image](/docs/images/Manual/common/filter/web/18.png){: width="800" }](/docs/images/Manual/common/filter/web/18.png){: target="_blank"}-->

<br />

## 16. 漏えい情報の選択
- 漏えい情報の有無別にログを選択して見ることができます。

<!-- [![image](/docs/images/Manual/common/filter/web/19.png){: width="800" }](/docs/images/Manual/common/filter/web/19.png){: target="_blank"}-->
 