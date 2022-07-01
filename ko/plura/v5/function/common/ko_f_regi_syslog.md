---
title: Syslog
permalink: ko_f_regi_syslog.html
sidebar: M_C
topnav: topnav
---

## 1. Syslog 필터 등록
- 버튼을 클릭하여 등록할 로그에 대한 상세 정보를 입력합니다.
- 적용된 추천 필터의 내용을 참고하세요.

     1-1. 필터분류 : 필터의 분류를 선택합니다.   
     1-2. 그룹 : 필터에 사용할 시스템 그룹을 선택합니다.   
     1-3. 운영체제 그룹 : 운영체제 종류를 선택합니다.   
     1-4. 채널 : OS별로 채널을 선택하여 필터를 등록할 수 있습니다.   
     1-5. 필터명 : 쉽게 알아볼 수 있는 이름으로 정합니다.   
     1-6. 필터위험도 : 필터의 위험도를 설정할 수 있습니다.   
     1-7. 필터상태 : 설정한 필터로 탐지한 로그를 필터탐지 메뉴에서 노출할 것인지를 설정할 수 있습니다.   
     1-8. 정보입력   
    - 1-8-1. 요소 선택 : 나열된 데이터 이름을 선택합니다.   
    - 1-8-2. 데이터 값 : 필터링을 필요로 하는 값을 입력합니다.   
    - 1-8-3. 포함 / 제외 : 필터링 시 입력값을 포함/제외 하여 알림을 받습니다.   

 <br />

아래는 등록 예시입니다.

[![image](/docs/images/Manual/common/filter2/syslog/1.png){: width="800" }](/docs/images/Manual/common/filter2/syslog/1.png){: target="_blank"}  

<br />
## 2. 필터탐지 조건 예시

**2-1.** 아래처럼 두 개 이상의 데이터 그룹이 있을 때, 그룹끼리는 AND 조건입니다.

[![image](/docs/images/Manual/common/filter2/syslog/2.png){: width="800" }](/docs/images/Manual/common/filter2/syslog/2.png){: target="_blank"}  
<br />

[![image](/docs/images/Manual/common/filter2/syslog/3.png){: width="800" }](/docs/images/Manual/common/filter2/syslog/3.png){: target="_blank"}  

<br />
**2-2.** 아래처럼 한 개의 그룹에 여러개의 데이터 값이 있을 때, 그룹 내의 값끼리는 OR 조건입니다.
[![image](/docs/images/Manual/common/filter2/syslog/4.png){: width="800" }](/docs/images/Manual/common/filter2/syslog/4.png){: target="_blank"}  


▣ 사용자정의 필터등록 DEMO : [https://qubitsec.github.io/ko_system_weblog.html](https://qubitsec.github.io/ko_system_weblog.html){: target="_blank"} 