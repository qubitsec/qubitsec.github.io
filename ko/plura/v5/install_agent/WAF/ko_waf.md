---
title: WAF Agent
permalink: ko_waf.html
sidebar: Install_A_W
product: Install_A_W
---
     
     PLURA WAF는 알려지지 않은(Unknown) 공격에 대응하기 위한 기능을 제공합니다.

     - 전체 로그 + 상세한 탐지 내역 제공 
     - 요청본문과 응답값 분석으로 크리덴셜스터핑 공격 대응 
     - 응답본문 분석으로 데이터유출 공격 대응 
     - SQL인젝션 완벽 차단 대응 

<br />

## 1. 사전 작업

PLURA 웹방화벽은 Amazon Linux 2 AMI(또는 CentOS 7)에 설치 가능합니다.

  - 1.1 웹방화벽을 설치할 EC2 인스턴스에 터미널 접속하여 root 권한을 획득한 후 설치를 진행
  - 1.2 타임존 설정 및 시간 동기화를 시스템에 맞게 설정

     `# timedatectl set-timezone Asia/Seoul`

     `# ntpdate time.google.com`

  - 1.3 방화벽 및 네트워크 보안 설정 

     - 80, 443 등 웹서비스에 사용되는 포트의 접속을 허용

<br />

## 2. 설치 작업

  - 2.1 SW 설치 명령

     `# curl https://repo.plura.io/v5/agent/install.sh | bash`

     `# /etc/plura/plura.sh install_waf`

  - 2.2 헬스체커 업로드 예외 설정 명령

     `# echo '[{"User-Agent": "ELB-HealthChecker/2.0"}]' > /etc/plura/conf/weblog-excluder.json`

  - 2.3 에이전트 등록 명령

     `# /etc/plura/plura.sh register [고객사 등록키]`


