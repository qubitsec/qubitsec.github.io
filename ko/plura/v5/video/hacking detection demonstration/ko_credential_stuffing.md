---
title: 크리덴셜 스터핑(Credential Stuffing)
permalink: ko_credential_stuffing.html
sidebar: Video_HD_testing
topnav: topnav
---

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/_LA7p-IeOOY' frameborder='0' allowfullscreen></iframe></div>

<br />

## 1. 크리덴셜 스터핑(Credential stuffing) 공격이란?

크리덴셜 스터핑(Credential stuffing)은 인터넷 사용자들이 동일한 로그인 정보(아이디와 비밀번호)를 여러 웹사이트나 서비스에서 사용하는 것에 대한 공격 방법입니다. 

크리덴셜 스터핑 공격은 해커가 일반적으로 공개된 또는 유출된 인증 정보(로그인 정보) 목록을 사용하여 대량으로 로그인 시도를 시도하는 것입니다. 

이 때, 대부분의 사이트들이 로그인 시도 횟수 제한 기능을 가지고 있기 때문에 공격자는 여러 개의 서버와 IP 주소를 사용하여 대규모의 로그인 시도를 할 수 있습니다.

<br />

## 2. 데모 공격 시나리오

  1) 모의공격을 통해 일정시간 동안 지속적으로 페이지 접속을 시도 (※ 모의공격 사용 도구 : Apache Jmeter)

  2) 공격 웹 로그가 PLURA에서 정상적으로 수집되었는지 확인

  3) PLURA 계정탈취 필터를 통해 크리덴셜 스터핑(Credential stuffing) 공격 탐지 확인

<br />

## 3. 참고사이트

  [1] 관리 > 보안 설정 [https://qubitsec.github.io/ko_manage_security.html](https://qubitsec.github.io/ko_manage_security.html){: target="_blank"}

  [2] ML탐지 [https://qubitsec.github.io/ko_ml.html](https://qubitsec.github.io/ko_ml.html){: target="_blank"}

  [3] 웹방화벽 > 방어 설정 [https://qubitsec.github.io/ko_defense_setting_waf.html](https://qubitsec.github.io/ko_defense_setting_waf.html){: target="_blank"}

  [4] 크리덴셜 스터핑 공격 대응하기 [http://blog.plura.io/?p=18955](http://blog.plura.io/?p=18955){: target="_blank"}

  [5] 웹 서비스 공격에 대응하기 [http://blog.plura.io/?p=18875](http://blog.plura.io/?p=18875){: target="_blank"}


