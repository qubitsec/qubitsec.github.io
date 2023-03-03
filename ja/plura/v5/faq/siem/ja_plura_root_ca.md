---
title: 私設Root証明書を登録する
permalink: ja_plura_root_ca.html
sidebar: faq_siem_M_ja
topnav: topnavja
---

<br />

## 1. PLURA Root CA 証明書の位置

- 以下のリンクに移動した後、証明書をパソコンに保存します。
[https://github.com/QubitSecurity/doc/blob/main/rocky8/sec/private-ssl-certificate/plura-rootca.crt](https://github.com/QubitSecurity/doc/blob/main/rocky8/sec/private-ssl-certificate/plura-rootca.crt){: target="_blank"}

- ブラウザ別の証明書登録手続きに従って進めてください。

<br />

## 2. ブラウザ別の私設Root証明書登録

### 2.1 Chrome

- 設定 > 個人情報保護およびセキュリティ > セキュリティ選択   
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/01.png){: width="800" }](/docs/images/Faq/siem/on-premise/plura_root_ca/01.png){: target="_blank"}-->

<br />

- 機器認証書の管理選択   
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/02.png){: width="800" }](/docs/images/Faq/siem/on-premise/plura_root_ca/02.png){: target="_blank"}-->

<br />

- 認証書 > 信頼できるルート認証機関タブへ移動 > インポートを選択
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/04.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/04.png){: target="_blank"}-->

<br />

- 証明書取得ウィザード > 次の選択   
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/05.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/05.png){: target="_blank"}-->

<br />

- 検索ボタンをクリックして登録する証明書の取得 > 次に選択 
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/07.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/07.png){: target="_blank"}-->

<br />

- 認証書情報を確認した後、ボタンをクリックしてください。  
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/09.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/09.png){: target="_blank"}-->

<br />

- セキュリティ警告 > はい、ボタンクリック
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/10.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/10.png){: target="_blank"}-->

<br />

- 認証書取得完了ポップアップ > 確認ボタンをクリック  
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/11.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/11.png){: target="_blank"}-->

<br />

### 2.2 Edge

- 設定 > 個人情報、検索及びサービス > 認証書管理の選択   
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/03.png){: width="800" }](/docs/images/Faq/siem/on-premise/plura_root_ca/03.png){: target="_blank"}-->

<br />

- 認証書 > 信頼できるルート認証機関タブへ移動 > インポートを選択  
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/04.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/04.png){: target="_blank"}-->

<br />

- 証明書取得ウィザード > 次の選択 
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/05.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/05.png){: target="_blank"}-->

<br />

- 検索ボタンをクリックして、登録する証明書の取得 > 次に選択
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/07.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/07.png){: target="_blank"}-->

<br />

- 認証書情報を確認した後、ボタンをクリックしてください。
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/09.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/09.png){: target="_blank"}-->

<br />

- セキュリティ警告 > はい、ボタンクリック  
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/10.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/10.png){: target="_blank"}-->

<br />

- 認証書取得完了ポップアップ > 確認ボタンをクリック
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/11.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/11.png){: target="_blank"}-->

<br />

### 2.3 Firefox

- 設定 > 個人情報およびセキュリティ > 認証書の表示ボタンをクリック  
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/12.png){: width="800" }](/docs/images/Faq/siem/on-premise/plura_root_ca/12.png){: target="_blank"}-->

<br />

- 認証書管理者 > 認証機関タブへ移動 > インポートボタンをクリック
- 登録したい証明書を取得します。
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/13.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/13.png){: target="_blank"}-->

<br />

- 認証書ダウンロード中 > 信頼された認証機関(ウェブサイト)チェックボックスを選択し、確認ボタンをクリック 
<!-- [![image](/docs/images/Faq/siem/on-premise/plura_root_ca/14.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/14.png){: target="_blank"}-->

<br />

<!-- ### 2.4 Safari -->

<!-- - Safari 追加 予定 -->
