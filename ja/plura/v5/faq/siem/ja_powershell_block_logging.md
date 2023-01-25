---
title: Powershell スクリプトブロックロギングオン
permalink: ja_powershell_block_logging.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

## 1. Windows PowerShell スクリプトブロックロギングオン映像

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/zbNXf4B__68' frameborder='0' allowfullscreen></iframe></div>

<br />

__映像チャプタープレビュー__

**00:38 ~ 01:10** → 01_PowerShell ver.5 以上の場合

**01:11 ~ 03:47** → 02_PowerShell 下位バージョンの場合(2012R2)

**03:48 ~ 04:00** → 03_PowerShell 下位バージョンの場合(その他OS)

<br />

## 2. Powershell Command

<br />

### 2-1. Powershell バージョン確認

`$PSVersionTable.PSVersion.Major`

<br />

### 2-2. Windows OS バージョン確認

`Get-WmiObject Win32_OperatingSystem | Select -Property Name`

<br />

### 2-3. PowerShell スクリプトブロックロギングオン “使用” (管理者権限で実行)

`reg add “HKLM\SOFTWARE\Policies\Microsoft\Windows\PowerShell\ScriptBlockLogging” /v “EnableScriptBlockLogging” /t REG_DWORD /d 1 /f`

<br />

### 2-4. PowerShellスクリプトブロックロギングオン “使用しない” (管理者権限で実行)

`reg delete “HKLM\SOFTWARE\Policies\Microsoft\Windows\PowerShell” /f`

<br />

### 2-5. PowerShellスクリプトブロックロギングオン “設定適用確認” (管理者権限で実行)

`reg query “HKLM\SOFTWARE\Policies\Microsoft\Windows\PowerShell\ScriptBlockLogging” /v “EnableScriptBlockLogging”`

<br />

WMF 5.1 インストール及び構成ダウンロードリンク

[https://docs.microsoft.com/ko-kr/powershell/scripting/windows-powershell/wmf/setup/install-configure?view=powershell-7](https://docs.microsoft.com/ko-kr/powershell/scripting/windows-powershell/wmf/setup/install-configure?view=powershell-7){:target="_blank"}