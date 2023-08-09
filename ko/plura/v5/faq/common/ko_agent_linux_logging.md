---
title: 리눅스 에이전트 로깅 설정
permalink: ko_agent_linux_logging.html
sidebar: faq_common_M
topnav: topnav
---

<br />

### 1. 로깅 디렉토리 변경

- 기존 : /var/log 
- (예시) 변경 : /sample

     에이전트 설치 후, 아래 순서대로 설정합니다.

     ``# mkdir /sample``   
     ``# mv -f /var/log/plura /sample/``   
     ``# ln -s /sample/plura /var/log/plura``   

<br />

### 2. 참고사항

- 용량 임계치의 경우, 호스트 당 임계치 설정이 가능하지만 특별히 관리 대상이 아니면 제한을 두지 않습니다.
- 로그보관주기 : 로컬 저장소 3시간


