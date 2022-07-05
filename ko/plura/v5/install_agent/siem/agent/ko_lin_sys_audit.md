---
title: Linux Syslog-Audit
permalink: ko_lin_sys_audit.html
sidebar: Install_A_S
product: Install_A_S
---

## Linux Agent Audit Log 활성화 영상

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/8WYGIsW08yY' frameborder='0' allowfullscreen></iframe></div>

<br />

## 1. Syslog Audit 활성화

- 아래 1-1, 1-2번 중 선택 사용

<br />

### 1-1. Audit Log 패키지 개별 설치

- CentOS, Red Hat, Amazon Linux   
`# yum -y install audit audisp-plugins`

- Ubuntu   
`# apt -y update`   
`# apt -y install auditd audispd-plugins`

<br />

사용자 환경에 따라 아래 패키지를 설치해주세요.

- CentOS, Red Hat, Amazon Linux   
`# yum -y install cronie logrotate rsyslog`

- Ubuntu   
`# apt -y update`   
`# apt -y install cron logrotate rsyslog`

<br />

### 1-2. Syslog+Audit 로그 패키지 통합 설치

- PLURA V5 Agent 사전 설치 필요
- 통합 설치   
`# /etc/plura/plura.sh install_syslog`

<br />

## 2. Audit 로그 확인

활성화 한 Audit로그는 다음의 메뉴에서 확인하실 수 있습니다.

- 필터탐지 > 시스템
- 전체로그 > 시스템
