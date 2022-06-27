---
title: Linux Syslog-Audit
permalink: lin_sys_audit.html
sidebar: Install_A_S
product: Install_A_S
---

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/8WYGIsW08yY' frameborder='0' allowfullscreen></iframe></div>

## 1. Syslog Audit 활성화(아래 1, 2번 중 선택 사용)

### 1.1 Audit Log 패키지 개별 설치를 진행합니다.

     ▶ CentOS, Red Hat, Amazon Linux
     # yum -y install audit audisp-plugins

     ▶ Ubuntu
     # apt -y update
     # apt -y install auditd audispd-plugins

     ※ 사용자 환경에 따라 아래 패키지를 설치해주세요.

     ▶ CentOS, Red Hat, Amazon Linux
     # yum -y install cronie logrotate rsyslog

     ▶ Ubuntu
     # apt -y update
     # apt -y install cron logrotate rsyslog

### 1.2 Syslog+Audit 로그 패키지 통합 설치를 진행합니다.

     ※ PLURA V5 Agent 사전 설치 필요

     # /etc/plura/plura.sh install_syslog

## 2. 활성화 한 Audit로그는 PLURA V5 웹 페이지에서 확인하실 수 있습니다.

  __필터탐지 > 시스템__

    전체로그 > 시스템

<br />
**참고 사이트**

– Audit 로그 중앙집중관리 [http://blog.plura.io/?p=5737](http://blog.plura.io/?p=5737){:target="_blank"}

– 오딧(Audit) 로그는 왜 필요한가요? [http://blog.plura.io/?page_id=7353](http://blog.plura.io/?page_id=7353){:target="_blank"}