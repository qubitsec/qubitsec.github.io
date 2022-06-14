---
title: PLURA V5 Syslog Collector for HP-UX Srv
permalink: p_sys_col_hp_ux_srv.html
sidebar: Install_G_S
product: Install_G_S
---

반드시 www.plura.io 우측 상단의 Install Agents 페이지에서 확인하여 설치하시길 바랍니다.

### 1. Syslog 를 전달받을 Linux 계열의 시스템에 PLURA V5 Agent를 설치합니다.

페이지 상단 메뉴에서 OS별 선택

  - CentOS/Ubuntu : Linux > Syslog 탭
 

### 2. HP-UX Srv 에서 Syslog 전송 설정을 합니다.

     # vi /etc/syslog.conf
     <예>
     *.info @로그취합 시스템 IP주소
     # /sbin/init.d/syslogd stop
     # /sbin/init.d/syslogd start

     @ 하나는 UDP로 통신
     @@ 두개는 TCP로 통신
     PLURA V5는 기본 @UDP 통신

### 3. www.plura.io 웹에서 시스템 등록을 합니다.
 **– 시스템 > 시스템 관리 > 취합 시스템 선택 > 시스템 등록**

 ![image](/docs/images/Ins_G/P_Sys_Collector_HP-UX_Srv/HP_UX.png){:class="align-center"}