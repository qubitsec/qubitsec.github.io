---
title: 웹
permalink: f_web.html
sidebar: M_C
topnav: topnav
---

     실시간으로 해킹 로그를 탐지하여 리스트를 보여주는 페이지입니다.
     PLURA V5 Agent는 클라이언트가 서버로 요청한 데이터를 GET방식과 POST방식으로 나누어 로그를 분석하여 공격유형,공격코드, 공격목적, 취약항목 등을 보여줍니다.
     탐지 가능 공격 유형은 OWASP TOP 10 입니다. 

<br />
바로가기  [웹 로그 사용 설정방법](https://qubitsec.github.io/system_weblog.html){: target="_blank"}

<br />
## 1. 탐지된 로그 상세 내용
- 탐지된 로그 목록을 클릭하면 각각의 로그에 담긴 자세한 내용들을 볼 수 있습니다.

[![image](/docs/images/Manual/common/filter/web/1.png){: width="800" }](/docs/images/Manual/common/filter/web/1.png){: target="_blank"}

<br />
 “재전송공격” 버튼은 재전송 공격의 조건이 성립한 경우에만 노출되므로 항상 보이지 않을 수 있습니다.

- 편집 버튼을 클릭하여 프로토콜&포트를 변경할 수 있습니다.(기본 설정은 https : 443)
- https를 사용하지 않는 경우, http : 80 으로 수정하여 재전송공격 데이터를 전송할 수 있습니다. 수정된 값은 저장됩니다.

[![image](/docs/images/Manual/common/filter/web/2.png)](/docs/images/Manual/common/filter/web/2.png){: target="_blank"}

<br />
- “curl://” 버튼 선택 시, 자동 복사(재전송 Query가 생성)가 되어 웹 전송 방식보다 더 많은 공격 옵션을 제공합니다.
※ “curl://” 공격 옵션 : 재전송 공격 + 모든 Method 포함(GET, POST, PUT, PATCH, DELETE, HEAD, OPTION, CONNECT, TRACE)

<br />
## 2. 탐지된 로그 원본 내용
- ‘로그상세’ 버튼을 클릭하면 발생된 원본 내용을 확인할 수 있습니다.

[![image](/docs/images/Manual/common/filter/web/3.png){: width="800" }](/docs/images/Manual/common/filter/web/3.png){: target="_blank"}

<br />
## 3. 컴플라이언스
- ‘컴플라이언스’ 버튼을 클릭하면 발생된 로그에 매칭되는 컴플라이언스 항목을 확인할 수 있습니다.

[![image](/docs/images/Manual/common/filter/web/4.png){: width="800" }](/docs/images/Manual/common/filter/web/4.png){: target="_blank"}


<br />
**데이터 유출** : 데이터 유출이 발생한 경우, 유출정보 항목에 표시가 됩니다.

[![image](/docs/images/Manual/common/filter/web/5.png){: width="800" }](/docs/images/Manual/common/filter/web/5.png){: target="_blank"}

<font color='dodgerblue'> ※ 데이터 유출 정보가 있는 경우에는 아래와 같이 유출정보 Tab이 추가되어 해당 내용을 확인할 수 있습니다. </font>

<br />
## 4. 데이터 유출 정보가 있는 경우, 탐지된 로그의 유출 정보
- 탐지된 로그 목록을 클릭 > 유출정보 Tab > 탐지된 로그의 유출 정보에 상세 내용들을 볼 수 있습니다.

[![image](/docs/images/Manual/common/filter/web/6.png){: width="800" }](/docs/images/Manual/common/filter/web/6.png){: target="_blank"}

- 탐지된 로그 목록을 클릭 > 유출정보 Tab > 응답본문 유출영역 보기 버튼 클릭
- 유출된 응답 본문에 대한 내용을 확인할 수 있습니다.

[![image](/docs/images/Manual/common/filter/web/7.png){: width="800" }](/docs/images/Manual/common/filter/web/7.png){: target="_blank"}

<br />
## 5. 전체로그 링크 – 마우스 우측 버튼
- 로그탐지 내역에서 마우스 우측 버튼을 클릭하면 시간대별 전체로그 페이지로 이동할 수 있습니다.
- 전체로그(=) : 탐지된 필터 탐지 내역과 **“동일한 시간대”**에 전체로그 페이지로 이동
- 전체로그(±1s) : 탐지된 필터 탐지 내역 **“1초”** 전후 시간대에 전체로그 페이지로 이동
- 전체로그(±5s) : 탐지된 필터 탐지 내역 **“5초”** 전후 시간대에 전체로그 페이지로 이동
- 전체로그(±60s) : 탐지된 필터 탐지 내역 **“60초”** 전후 시간대에 전체로그 페이지로 이동

[![image](/docs/images/Manual/common/filter/web/8.png){: width="800" }](/docs/images/Manual/common/filter/web/8.png){: target="_blank"}

<br />
## 6. 항목별 정렬
- 날짜/요청크기/응답크기/동일로그 기준으로 정렬할 수 있습니다.

[![image](/docs/images/Manual/common/filter/web/9.png){: width="800" }](/docs/images/Manual/common/filter/web/9.png){: target="_blank"}
 
<br />
## 7. 페이지당 로그 수
- 한 페이지당 보이는 로그의 수를 20개, 30개, 40개, 50개로 설정할 수 있습니다.

[![image](/docs/images/Manual/common/filter/web/10.png){: width="800" }](/docs/images/Manual/common/filter/web/10.png){: target="_blank"}

<br />
## 8. 날짜/시간 선택
- 지난 날짜와 시간을 선택하여 로그를 볼 수 있습니다.

 [![image](/docs/images/Manual/common/filter/web/11.png){: width="800" }](/docs/images/Manual/common/filter/web/11.png){: target="_blank"}

<br />
## 9. 그룹 선택
- 사용자가 등록한 시스템 그룹을 선택해서 볼 수 있습니다.

[![image](/docs/images/Manual/common/filter/web/12.png){: width="800" }](/docs/images/Manual/common/filter/web/12.png){: target="_blank"}

 <br />
## 10. 운영체제 선택
- 운영체제를 선택해서 볼 수 있습니다.

[![image](/docs/images/Manual/common/filter/web/13.png){: width="800" }](/docs/images/Manual/common/filter/web/13.png){: target="_blank"}

<br />
## 11. 시스템 IP주소 선택
- 원하는 시스템 IP주소를 선택해서 볼 수 있습니다.

[![image](/docs/images/Manual/common/filter/web/14.png){: width="800" }](/docs/images/Manual/common/filter/web/14.png){: target="_blank"}
 
<br />
## 12. 분류 선택
- 분류별로 선택해서 볼 수 있습니다.

[![image](/docs/images/Manual/common/filter/web/15.png){: width="800" }](/docs/images/Manual/common/filter/web/15.png){: target="_blank"}
 
<br />
## 13. 코드 선택
- OWASP TOP10 에 선정된  취약점별로 선택해서 볼 수 있습니다.

[![image](/docs/images/Manual/common/filter/web/16.png){: width="800" }](/docs/images/Manual/common/filter/web/16.png){: target="_blank"}
 
<br />
## 14. 위험도 선택
- 위험도를 선택하여 볼 수 있습니다.

[![image](/docs/images/Manual/common/filter/web/17.png){: width="800" }](/docs/images/Manual/common/filter/web/17.png){: target="_blank"}
 
<br />
## 15. 상태값 선택
- 상태값을 선택하여 볼 수 있습니다.


 [![image](/docs/images/Manual/common/filter/web/18.png){: width="800" }](/docs/images/Manual/common/filter/web/18.png){: target="_blank"}

<br />
## 16. 유출정보 선택
- 유출정보 유무별로 로그를 선택하여 볼 수 있습니다.

[![image](/docs/images/Manual/common/filter/web/19.png){: width="800" }](/docs/images/Manual/common/filter/web/19.png){: target="_blank"}
 