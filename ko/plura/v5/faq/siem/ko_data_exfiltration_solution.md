---
title: 데이터유출
permalink: ko_data_exfiltration_solution.html
sidebar: faq_siem_M
topnav: topnav
---

데이터 유출 탐지 예외사항과 해결책에 대해 알아보겠습니다.

<br />

## 1. Content-Type : MIME 타입 검사

※ MIME 타입이란, 클라이언트에게 전송된 문서의 다양성을 알려주기 위한 메커니즘입니다.

### 1.1. PLURA V5에서는 오직 아래의 타입인 경우에만 동작합니다.

  **text**

     텍스트를 포함하는 모든 문서를 나타내며 이론상으로는 인간이 읽을 수 있어야 합니다.
     예시) text/plain, text/html, text/css, text/javascript

<br />

  **멀티 타입**

     멀티파트 타입은 일반적으로 다른 MIME 타입들을 지닌 개별적인 파트들로 나누어지는 문서의 카테고리를 가리킵니다.

 <br />

## 2. Content-Encoding

 PLURA V5에서는 압축 해제(Disable Compression) 문제로 예외 처리(검사하지 않음)

<br />

## 3. charset=UTF-8

※ <meta> 태그의 charset 속성은 해당 HTML 문서의 문자 인코딩 방식을 명시합니다.

 PLURA V5에서는 UTF-8 에서만 동작합니다.<font color='dodgerblue'> (Windows-IIS의 경우) </font>

<br />

### 3-1. 응답본문 선택 시, 만나는 에러 문구

 필터 탐지는 되었으나 응답본문 내용을 읽을 수 없을 경우, 아래의 문구가 노출됩니다.

[![image](/docs/images/Additianal/data/1.png)](/docs/images/Additianal/data/1.png){: target="_blank"}

<br />

### 3-2. 문제점

 응답본문 문자 인코딩이 UTF-8 이 아닌, 한글 인코딩과 같이 멀티바이트(multi-byte) 인코딩으로 되어 있을 경우 발생됩니다.

<br />

### 3-3. 해결책

 응답본문이 UTF-8 으로 응답할 수 있도록 웹 문서에 아래 태그를 삽입해주세요.


**<meta charset=”UTF-8″>**

[![image](/docs/images/Additianal/data/2.png)](/docs/images/Additianal/data/2.png){: target="_blank"}

<br />

 웹 문서 저장시 인코딩을 UTF-8 으로 저장해주세요.

[![image](/docs/images/Additianal/data/3.png)](/docs/images/Additianal/data/3.png){: target="_blank"}

<br />

## 4. MIME 타입 정리

MIME 타입은 개별 타입과 멀티파트 타입으로 구분됩니다.

 **개별 타입**
      text/plain
      text/html
      image/jpeg
      image/png
      audio/mpeg
      audio/ogg
      audio/*
      video/mp4
      application/octet-stream
      …

 개별타입은 문서의 카테고리를 가리키며, 다음 중 하나가 될 수 있습니다.

[![image](/docs/images/Additianal/data/4.png){: width="800" }](/docs/images/Additianal/data/4.png){: target="_blank"}

<br />

     특정 서브타입이 없는 텍스트 문서들에 대해서는 text/plain 이 사용되어야 합니다.
     특정 혹은 알려진 서브타입이 없는 이진 문서에 대해서는 유사하게, application/octet-stream이 사용되어야 합니다.

<br />

**멀티파트 타입**

     multipart/form-data
     multipart/byteranges

     멀티파트 타입은 일반적으로 다른 MIME 타입들을 지닌 개별적인 파트들로 나누어지는 문서의 카테고리를 가리킵니다.
     즉, 이 타입은 합성된 문서를 나타내는 방법입니다.
     HTML Forms 과 POST 메서드의 관계 속에서 사용되는 multipart/form-data, 그리고 전체 문서의 하위 집합만 전송하기 위한 206 Partial Content 상태 메시지와 함께 사용되는 multipart/byteranges 를 제외하고는, HTTP 가 멀티파트 문서를 다룰 수 있는 특정한 방법은 존재하지 않습니다 : 메시지는 브라우저에 간단히 전달됩니다.(문서를 인라인에 어떻게 디스플레이할지 모르기에, ‘다른 이름으로 저장’ 윈도우를 제시할 겁니다.)

<br />

참고 사이트

 1. Content-Type : MIME 타입 검사 [https://mzl.la/327am7k](https://mzl.la/327am7k){: target="_blank"}

 2. Content-Encoding [https://bit.ly/31ecOJW](https://bit.ly/31ecOJW){: target="_blank"}

 3. charset=UTF-8 [https://theqoop.tistory.com/266](https://theqoop.tistory.com/266){: target="_blank"}

 4. Apache 서버에서 HTTP 압축 비활성화 [https://qubitsec.github.io/ko_apache_http_compression.html](https://qubitsec.github.io/ko_apache_http_compression.html){: target="_blank"}