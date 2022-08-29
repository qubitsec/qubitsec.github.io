---
title: 재전송공격 사용법 안내 
permalink: ko_hack_re_attack.html
sidebar: faq_siem_M
topnav: topnav
---

### 1. PLURA V5 Manual – 재전송 공격 영상

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/_ICFu8Rg5h0' frameborder='0' allowfullscreen></iframe></div>

<br />

**재전송공격**이란, 탐지 로그를 이용하여 실제 공격을 확인하는 기능으로 모의해킹의 일환입니다.

**재전송공격**으로 모의 해킹을 하는 이유는 공격의 성공과 실패를 확인하기 위함입니다.
SQL 인젝션 공격의 성공은 매우 심각한 위험에 노출되므로 성공에 대하여 반드시 확인해야 하지만,
수많은 공격 로그 중에서 모의해킹을 테스트하기가 매우 어렵습니다.

프루라의 재전송공격은 이러한 불편함을 제거하고 업무 효율의 극대화를 위하여 제공하고 있습니다.

“**재전송공격**” 버튼은 재전송 공격의 조건이 성립한 경우에만 노출되므로 항상 보이지 않을 수 있습니다.

또한, 사용자 브라우저에서 진행되므로 해당 호스트(Host), URL 에 접근할 수 있는 네트워크 환경이어야만 제대로 동작할 수 있습니다. 즉, 네트워크 환경에 영향을 받습니다.

<br />

### 2. HTTP Method 재전송 대상

2-1. GET 모든 로그

2-2.
POST | PUT | PATCH | DELETE 의 경우 파라미터 이름이 존재하면서 Content-type 이 존재하는 로그

<br />

### 3. Content-Type 재전송 대상

3-1. application/x-www-form-urlencoded : key/value 형태

3-2. application/json : json 형태

3-3. application/xml :xml 형태

아래의 이미지는 Method – GET 방식(application/x-www-form-urlencoded) 의 공격으로 재전송 공격의 조건이 성립되어 재전송공격 버튼이 노출된 것을 확인할 수 있습니다.

로그 예시 : 필터탐지 > 웹

 [![image](/docs/images/Additianal/hack/1.png){: width="800" }](/docs/images/Additianal/aws/1.png){: target="_blank"}

<br />

편집 버튼을 클릭하여 프로토콜&포트를 변경 할 수 있습니다.(기본 설정은 https : 443)

https 를 사용하지 않는 경우, http : 80 으로 수정하여 재전송공격 데이터를 전송할 수 있습니다.
수정된 값은 저장됩니다.

 [![image](/docs/images/Additianal/hack/2.png)](/docs/images/Additianal/aws/2.png){: target="_blank"}
 
 <br />

**“curl://” 버튼** 선택 시, 자동 복사(재전송 Query가 생성)가 되어 웹 전송 방식보다 더 많은 공격 옵션을 제공합니다.

※ **“curl://” 공격 옵션 :** 재전송 공격 + 모든 Method 포함(GET, POST, PUT, PATCH, DELETE, HEAD, OPTION, CONNECT, TRACE)

<br />

### 4. HTTP Method 재전송 대상이 아닌 경우 – 재전송공격 버튼 미노출

4-1. POST (상단 재전송 가능 조건이 만족하지 않는 경우)

4-2. PUT (상단 재전송 가능 조건이 만족하지 않는 경우)

4-3. PATCH (상단 재전송 가능 조건이 만족하지 않는 경우)

4-4. DELETE (상단 재전송 가능 조건이 만족하지 않는 경우)

4-5. HEAD

4-6. OPTION

4-7. CONNECT

4-8. TRACE

<br />

### 5. Content-Type 재전송 대상이 아닌 경우 – 재전송공격 버튼 미노출

5-1. multipart/form-data : key/value 형태 (바이너리 포함)

5-2. application/octet-stream : 바이너리 파일

5-3. text/yaml : yml
