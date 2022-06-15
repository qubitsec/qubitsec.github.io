---
title: PLURA V5 AgentLinux Srv
permalink: p_agent_lin_srv.html
sidebar: Install_G_S
product: Install_G_S
---



아래의 내용은 CentOS 7 버전 설치 과정 예시 입니다.
반드시 www.plura.io 우측 상단의 Install Agents 페이지에서 확인하여 설치하시길 바랍니다.


__◆ PLURA V5 Linux Syslog 설치 영상__

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/TW7_NF1gF9g' frameborder='0' allowfullscreen></iframe></div>



## 1. PLURA V5 Agent를 설치합니다.


     - [root@localhost]# sudo -s
     - [root@localhost]# curl https://repo.plura.io/v5/agent/install.sh | bash

## 2. 라이센스 등록 및 실행 합니다.

     - [root@localhost]# /etc/plura/plura.sh register ****


## 3. 설치 정보를 확인합니다.

     - [root@localhost]# /etc/plura/pluraagent -version
     - Version: x.x.x


__◆ PLURA V5 Agent Linux Srv 설치 영상__

– Linux Syslog 설치 영상 : [http://blog.plura.io/?p=11344](http://blog.plura.io/?p=11344){:target="_blank"}

– Linux Syslog-Audit 설치 영상 : [http://blog.plura.io/?p=13228](http://blog.plura.io/?p=13228){:target="_blank"}

– Linux Apache / Nginx 설치 영상 : [http://blog.plura.io/?p=11347](http://blog.plura.io/?p=11347){:target="_blank"}

– Linux Web Server – Datos 설치 영상 : [http://blog.plura.io/?p=11351](http://blog.plura.io/?p=11351){:target="_blank"}




## 4. 추가 설정이 필요하면 아래와 같이 파일을 추가합니다.


설치 경로를 선택할 수 있습니다.


     [root@localhost]# vi /etc/plura/conf/plura.conf

     # 시스템 기동 시 에이전트 로그인 지연 설정
     login_delay_sec = 0 (초)

     # AWS 환경에서 Auto Scaling 사용 시 인스턴스 고유의 식별자를 PLURA V5 시스템으로 전송하는 설정(값이 1일때 전송)
     login_with_machine_id = 0

     # 여러개의 네트워크 인터페이스를 사용할 때 PLURA V5 웹에 표시되는 IP주소 설정
       interface = eth1 (시스템 > 시스템 관리 리스트에 보이는 대표 IP주소를 지정)
       interface_mon = eth1 (시스템 > 리소스 모니터링 > 네트워크 트래픽을 수집 할 인터페이스 설정)


     # 시스템 기동 시 hostname 변경에 따른 로그인 지연 설정
       login_hostname_check=0 (default = 0)
     # 0 > 지정된 지연시간까지 무조건 기다림
     # 1 > hostname 변경이 1회 감지되면 지연 중단
     # 2 > hostname 변경이 2번 감지되면 지연 중단




__5. CentOS 6 End of Lifetime (EOL) 대응__

     에이전트 설치 전에 아래 명령을 실행

     # mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.org

     * CentOS Product Specifications
       https://wiki.centos.org/About/Product

       제조사가 지원을 종료한 제품에 대하여 PLURA V5에서도 지원을 종료합니다.
       PLURA V5에서 지원하지 않는 운영체제 버전을 사용한다면 문제가 발생할 수 있습니다.
       제조사가 지원 종료한 버전을 사용 중이라면 업그레이드에 대하여 보다 적극적인 검토가 필요합니다. 해킹과 장애 등 다양한 문제에 직면하고 심각한 문제로 발전할 수 있기 때문입니다.
