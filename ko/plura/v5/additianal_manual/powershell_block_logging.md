---
title: Powershell 스크립트 블록 로깅 켜기
permalink: powershell_block_logging.html
sidebar: Add_M
topnav: topnav
---

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/zbNXf4B__68' frameborder='0' allowfullscreen></iframe></div>


- 동영상 챕터 요약

– **00:38 ~ 01:10** → 01_PowerShell ver.5 이상인 경우

– **01:11 ~ 03:47** → 02_PowerShell 하위버전인 경우(2012R2)

– **03:48 ~ 04:00** → 03_PowerShell 하위버전인 경우(그 외 OS)


- Powershell Command

**– Powershell 버전 확인 :**

     $PSVersionTable.PSVersion.Major

**– Windows OS 버전 확인 :**

     Get-WmiObject Win32_OperatingSystem | Select -Property Name

**– PowerShell 스크립트 블록 로깅 켜기 “사용” (관리자 권한으로 실행) :**

     reg add “HKLM\SOFTWARE\Policies\Microsoft\Windows\PowerShell\ScriptBlockLogging” /v “EnableScriptBlockLogging” /t REG_DWORD /d 1 /f

**– PowerShell 스크립트 블록 로깅 켜기 “사용안함” (관리자 권한으로 실행) :**

     reg delete “HKLM\SOFTWARE\Policies\Microsoft\Windows\PowerShell” /f

**– PowerShell 스크립트 블록 로깅 켜기 “설정 적용확인” (관리자 권한으로 실행) :**

     reg query “HKLM\SOFTWARE\Policies\Microsoft\Windows\PowerShell\ScriptBlockLogging” /v “EnableScriptBlockLogging”


- WMF 5.1 설치 및 구성 다운로드 링크

[https://docs.microsoft.com/ko-kr/powershell/scripting/windows-powershell/wmf/setup/install-configure?view=powershell-7](https://docs.microsoft.com/ko-kr/powershell/scripting/windows-powershell/wmf/setup/install-configure?view=powershell-7){:target="_blank"}