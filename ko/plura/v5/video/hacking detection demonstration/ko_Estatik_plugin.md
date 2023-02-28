---
title: Estatik plugin vulnerability
permalink: ko_Estatik_plugin.html
sidebar: Video_HD_testing
topnav: topnav
---

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/fNhVYHjSKdQ' frameborder='0' allowfullscreen></iframe></div>

<br />

## 1. Estatik plugin vulnerability

워드프레스 Estatik plugin은 워드프레스 부동산 웹사이트를 구성할 수 있는 플러그인입니다.

2.2.1버전에 업로드 함수에서 파일 확장자 체크를 하는 로직이 존재하지 않아, 워드프레스에서 제공하는 에이잭스(ajax)의 잘못된 사용으로 파일 업로드 취약점이 발생하였습니다.

<br />

## 2. 데모 공격 시나리오

  1) Estatik plugin 취약점을 이용한 파일 업로드 공격

  2) 공격로그가 PLURA에서 정상적으로 수집되었는지 확인

  3) PLURA 웹방화벽 로그를 활용한 분석 방법 

  4) PLURA 웹방화벽(WAF)- Estatik plugin 취약점 공격에 대한 차단 시연

<br />

## 3. 참고사이트
  
  [1] 워드프레스로 만든 사이트 필수 보안 TOP 10 [http://blog.plura.io/?p=18623](http://blog.plura.io/?p=18623){: target="_blank"}

  