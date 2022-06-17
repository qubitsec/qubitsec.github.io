---
title: 검색기능
permalink: search_fun.html
sidebar: M_C
topnav: topnav
---

     페이지별 우측 상단의 도움말을 클릭하시면 각 로그에 대한 설명이 안내되어 있습니다.
     문자열, 숫자별로 다양한 검색이 가능합니다.

#### ◆ 검색 방법 간단 TIP

     2019-04-30T06:21:25* : 2019-04-30T-6:21:25로 시작되는 모든 정보 검색
     검색 추가 : AND 검색 가능
     검색 개인화 : 검색 조건의 개인화

#### ◆ 메뉴별 검색 방법 간단 TIP

     필터탐지 페이지 : 필터명, 자세히보기 xml 기준 일부분 검색 가능
     로그조회 페이지 : 자세히보기 xml 기준으로 일부분 검색 가능
     필터관리 : 이벤트타입, 필터명 검색 가능
     IP주소 추출 : IP, 국가, 추출일 검색 가능
     시스템 관리 : 시스템 IP, 호스트명, 등록일 검색 가능

     검색 기능은 검색창에  찾고싶은 검색어를 입력하거나 자세히보기의 XML을 기반으로 원하는 문구를 copy&paste 하여 검색할 수 있습니다.
     아래와 같은 방법으로 검색기능을 활용할 수 있습니다.

#### ◆ 문자열 검색 시, “포함”, “일치”, “제외”, “포함제외” 항목 선택이 가능합니다.

[![image](/docs/images/Manual/common/search/1.png)](/docs/images/Manual/common/search/1.png){: target="_blank"}

#### ◆ 숫자 검색 항목 선택 시, 연산 기호 선택이 가능합니다. 

[![image](/docs/images/Manual/common/search/2.png)](/docs/images/Manual/common/search/2.png){: target="_blank"}

#### ◆ 검색 조건에 대하여 개인화 설정(적용, 미적용, 고정)이 가능합니다.

     – Full Log에서 “wordpress”라는 문자열이 포함되고, logStatus 값이 200이상인 로그 검색을 고정하여 사용하고 싶은 경우, 아래와 같이 검색합니다.
     – 검색개인화 영역에서 고정 버튼을 선택합니다.

[![image](/docs/images/Manual/common/search/3.png)](/docs/images/Manual/common/search/3.png){: target="_blank"}


#### ◆ 로그 조회 시, 우측 마우스 동작으로 링크 제공

[![image](/docs/images/Manual/common/search/4.png)](/docs/images/Manual/common/search/4.png){: target="_blank"}


#### ◆ 타이머 기능 : 검색 조건이 추가되는 경우, 우측 상단에 타이머가 노출

[![image](/docs/images/Manual/common/search/5.png)](/docs/images/Manual/common/search/5.png){: target="_blank"}

     – 대상 라이센스: Enterprise(On-Prem), Premium에 제공
     – 전체로그, 필터탐지, ML탐지 페이지에 노출

     – 타이머가 종료되면 페이지가 새로고침되어 데이터를 갱신합니다.
     – 검색 시간 설정(30s, 60s, 90s, 120s)을 변경할 수 있습니다.

[![image](/docs/images/Manual/common/search/6.png)](/docs/images/Manual/common/search/6.png){: target="_blank"}

#### ◆  다음은 로그 검색에 관한 예시입니다.

     – 응답사이즈가 10000 이상이고, logURI 값이 /wordpress/index.php인 로그 검색을 원하는 경우, 아래와 같이 검색합니다.

[![image](/docs/images/Manual/common/search/7.png)](/docs/images/Manual/common/search/7.png){: target="_blank"}

#### ◆ 다음은 필터탐지 로그 검색에 관한 예제 입니다.

     – 로그인에 대한  탐지만 보기를 원할 때   “로그인” 이라는 단어를 입력합니다.
     로그인과 관련된 필터 탐지 내용을 볼 수 있습니다.

[![image](/docs/images/Manual/common/search/8.png)](/docs/images/Manual/common/search/8.png){: target="_blank"}


 