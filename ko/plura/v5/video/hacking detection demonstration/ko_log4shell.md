---
title: Log4Shell
permalink: ko_log4shell.html
sidebar: Video_HD_testing
topnav: topnav
---

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/9YtI-plPXm8' frameborder='0' allowfullscreen></iframe></div>

<br />

## 1. Log4Shell이란?

Log4Shell 또는 CVE-2021-44228는 저명한 자바 로깅 프레임워크 Log4j의 제로 데이 임의 코드 실행 취약점입니다.

이 취약점은 알리바바의 클라우드 보안팀에 의해 2021년 11월 24일 아파치에 비공개로 전달되었으며 2021년 12월 9일 대중에게 공개되었습니다.

이 취약점은 LDAP과 JNDI 요청을 검사하지 않는 Log4j의 특징을 이용하여, 공격자가 임의의 자바 코드를 서버 또는 기타 컴퓨터에서 실행할 수 있게 합니다.

Log4j 프로젝트를 맡는 아파치 소프트웨어 재단은 Log4Shell에 CVSS 점수 최고점인 10점을 부여하였습니다.

<br />

## 2. 데모 공격 시나리오

  1) 취약한 Log4Shell를 사용하는 Victim 웹서비스에 접근하여 payload를 전송

  2) /etc/passwd 정보탈취
  
  3) 공격로그가 PLURA에서 정상적으로 수집되었는지 확인
  
  4) PLURA 웹방화벽(WAF) - Log4Shell 공격에 대한 차단 시연

<br />

## 3. 참고사이트

  [1] Log4shell [http://blog.plura.io/?p=17912](http://blog.plura.io/?p=17912){: target="_blank"}

  [2] CVE-2021-44228 (Log4Shell) Apache Log4j 보안 취약점 대응 : [http://blog.plura.io/?p=16659](http://blog.plura.io/?p=16659){: target="_blank"}

  [3] Apache Log4j 취약점 (CVE-2021-44228) 업데이트 안내 : [http://blog.plura.io/?p=16723](http://blog.plura.io/?p=16723){: target="_blank"}
