---
title: 사설 Root 인증서 등록하기
permalink: ko_plura_root_ca.html
sidebar: faq_siem_M
topnav: topnav
---

<br />

## 1. PLURA Root CA 인증서 위치

- 아래 링크로 이동한 뒤, 인증서를 PC에 저장합니다.
[https://github.com/QubitSecurity/doc/blob/main/rocky8/sec/private-ssl-certificate/plura-rootca.crt](https://github.com/QubitSecurity/doc/blob/main/rocky8/sec/private-ssl-certificate/plura-rootca.crt){: target="_blank"}

- 브라우저별 인증서 등록 절차에 따라 진행해주세요.

<br />

## 2. 브라우저별 사설 Root 인증서 등록

### 2.1 Chrome

- 설정 > 개인정보 보호 및 보안 > 보안 선택   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/01.png){: width="800" }](/docs/images/Faq/siem/on-premise/plura_root_ca/01.png){: target="_blank"}

<br />

- 기기 인증서 관리 선택   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/02.png){: width="800" }](/docs/images/Faq/siem/on-premise/plura_root_ca/02.png){: target="_blank"}

<br />

- 인증서 > 신뢰할 수 있는 루트 인증기관 탭 이동 > 가져오기 선택
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/04.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/04.png){: target="_blank"}

<br />

- 인증서 가져오기 마법사 > 다음 선택   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/05.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/05.png){: target="_blank"}

<br />

- 찾아보기 버튼 클릭하여, 등록할 인증서 가져오기 > 다음 선택   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/07.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/07.png){: target="_blank"}

<br />

- 모든 인증서를 다음 저장소에 저장(신뢰할 수 있는 루트 인증 기관) 체크박스 선택 > 다음 선택
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/15.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/15.png){: target="_blank"}

<br />

- 인증서 정보 확인 후, 마침 버튼 클릭   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/09.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/09.png){: target="_blank"}

<br />

- 보안 경고 > 예 버튼 클릭   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/10.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/10.png){: target="_blank"}

<br />

- 인증서 가져오기 완료 팝업 > 확인 버튼 클릭   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/11.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/11.png){: target="_blank"}

<br />

### 2.2 Edge

- 설정 > 개인정보, 검색 및 서비스 > 인증서 관리 선택   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/03.png){: width="800" }](/docs/images/Faq/siem/on-premise/plura_root_ca/03.png){: target="_blank"}

<br />

- 인증서 > 신뢰할 수 있는 루트 인증기관 탭 이동 > 가져오기 선택  
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/04.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/04.png){: target="_blank"}

<br />

- 인증서 가져오기 마법사 > 다음 선택   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/05.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/05.png){: target="_blank"}

<br />

- 찾아보기 버튼 클릭하여, 등록할 인증서 가져오기 > 다음 선택   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/07.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/07.png){: target="_blank"}

<br />

- 모든 인증서를 다음 저장소에 저장(신뢰할 수 있는 루트 인증 기관) 체크박스 선택 > 다음 선택
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/15.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/15.png){: target="_blank"}

<br />

- 인증서 정보 확인 후, 마침 버튼 클릭   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/09.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/09.png){: target="_blank"}

<br />

- 보안 경고 > 예 버튼 클릭   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/10.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/10.png){: target="_blank"}

<br />

- 인증서 가져오기 완료 팝업 > 확인 버튼 클릭   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/11.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/11.png){: target="_blank"}

<br />

### 2.3 Firefox

- 설정 > 개인 정보 및 보안  > 인증서 보기 버튼 클릭   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/12.png){: width="800" }](/docs/images/Faq/siem/on-premise/plura_root_ca/12.png){: target="_blank"}

<br />

- 인증서 관리자 > 인증기관 탭 이동 > 가져오기 버튼 클릭 
- 등록하고자 하는 인증서를 가져옵니다.
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/13.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/13.png){: target="_blank"}

<br />

- 인증서 다운로드 중 > 신뢰된 인증 기관(웹 사이트) 체크박스 선택 후, 확인 버튼 클릭   
[![image](/docs/images/Faq/siem/on-premise/plura_root_ca/14.png)](/docs/images/Faq/siem/on-premise/plura_root_ca/14.png){: target="_blank"}

<br />

<!-- ### 2.4 Safari -->

<!-- - Safari 추가 예정 -->
