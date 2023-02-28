---
title: 사이트 간 스크립팅(XSS)
permalink: ko_xss.html
sidebar: Video_HD_testing
topnav: topnav
---

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/dfbZ6_tWthA' frameborder='0' allowfullscreen></iframe></div>

<br />

## 1. 사이트 간 스크립팅(XSS)

웹 애플리케이션에서 많이 나타나는 취약점의 하나로 웹사이트 관리자가 아닌 이가 웹 페이지에 악성 스크립트를 삽입할 수 있는 취약점입니다.

주로 여러 사용자가 보게 되는 전자 게시판에 악성 스크립트가 담긴 글을 올리는 형태로 이루어집니다. 

이 취약점은 웹 애플리케이션이 사용자로부터 입력 받은 값을 제대로 검사하지 않고 사용할 경우 나타납니다. 

이 취약점으로 해커가 사용자의 정보(쿠키, 세션 등)를 탈취하거나, 자동으로 비정상적인 기능을 수행하게 할 수 있습니다. 

주로 다른 웹사이트와 정보를 교환하는 식으로 작동하므로 사이트 간 스크립팅이라고 합니다.

<br />

## 2. 데모 공격 시나리오
  
  1) 사이트 간 스크립팅(XSS) 공격 실행
  
  2) 공격로그가 PLURA에서 정상적으로 수집되었는지 확인
  
  3) PLURA 웹 필터를 활용한 분석 방법 

<br />

## 3. 참고사이트

  [1] XSS 대응방안 [http://blog.plura.io/?p=7614](http://blog.plura.io/?p=7614){: target="_blank"}

  [2] Q&A 게시판, 정성스레 적힌 질문 그 뒤에 숨겨진 XSS 공격 [http://blog.plura.io/?p=6923](http://blog.plura.io/?p=6923){: target="_blank"}


