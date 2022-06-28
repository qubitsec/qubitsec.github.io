---
title: 필터탐지 (웹방화벽)
permalink: filter_detection_waf.html
sidebar: M_WAF
topnav: topnav
---



      실시간으로 웹방화벽 탐지 리스트를 보여주는 페이지입니다.

<br />
## 1.탐지된 로그 상세 내용

- 탐지된 로그 목록을 클릭하면 각각의 로그에 담긴 자세한 내용들을 볼 수 있습니다.

[![image](/docs/images/Manual/waf/filter_detec/1.png){: width="800" }](/docs/images/Manual/waf/filter_detec/1.png){: target="_blank"}

<br />
## 2.탐지된 로그 원본 내용

- ‘로그상세’ 버튼을 클릭하면 발생된 원본 내용을 확인할 수 있습니다.

[![image](/docs/images/Manual/waf/filter_detec/2.png){: width="800" }](/docs/images/Manual/waf/filter_detec/2.png){: target="_blank"}

<br />
## 3.데이터 유출 

- 데이터 유출이 발생한 경우, 유출정보 항목에 표시가 됩니다.

[![image](/docs/images/Manual/waf/filter_detec/3.png){: width="800" }](/docs/images/Manual/waf/filter_detec/3.png){: target="_blank"}

<font color='dodgerblue'>※ 데이터 유출 정보가 있는 경우에는 아래와 같이 유출정보 Tab이 추가되어 해당 내용을 확인할 수 있습니다.</font>

<br />
## 4.데이터 유출 정보가 있는 경우, 탐지된 로그의 유출 정보

- 탐지된 로그 목록을 클릭 > 유출정보 Tab > 탐지된 로그의 유출 정보에 상세 내용들을 볼 수 있습니다.

[![image](/docs/images/Manual/waf/filter_detec/4.png){: width="800" }](/docs/images/Manual/waf/filter_detec/4.png){: target="_blank"}

- 탐지된 로그 목록을 클릭 > 유출정보 Tab > 응답본문 유출영역 보기 버튼 클릭
- 유출된 응답 본문에 대한 내용을 확인할 수 있습니다.

<br />
[![image](/docs/images/Manual/waf/filter_detec/5.png)](/docs/images/Manual/waf/filter_detec/5.png){: target="_blank"}

<br />
## 5.전체로그 링크(마우스 우측 버튼)

- 로그탐지 내역에서 마우스 우측 버튼을 클릭하면 시간대별 전체로그 페이지로 이동할 수 있습니다.

- 전체로그(=) : 탐지된 필터 탐지 내역과 “동일한 시간대”에 전체로그 페이지로 이동

- 전체로그(±1s) : 탐지된 필터 탐지 내역 “1초” 전후 시간대에 전체로그 페이지로 이동

- 전체로그(±5s) : 탐지된 필터 탐지 내역 “5초” 전후 시간대에 전체로그 페이지로 이동

- 전체로그(±60s) : 탐지된 필터 탐지 내역 “60초” 전후 시간대에 전체로그 페이지로 이동

[![image](/docs/images/Manual/waf/filter_detec/6.png){: width="800" }](/docs/images/Manual/waf/filter_detec/6.png){: target="_blank"}

<br />
## 6.항목별 정렬
- 생성일/요청사이즈/응답사이즈/동일로그 기준으로 최신순과 오래된순으로 정렬할 수 있습니다.

[![image](/docs/images/Manual/waf/filter_detec/7.png){: width="800" }](/docs/images/Manual/waf/filter_detec/7.png){: target="_blank"}

<br />
## 7.페이지당 로그 수
- 한 페이지당 보이는 로그의 수를 20개, 30개, 40개, 50개 로 설정할 수 있습니다.

[![image](/docs/images/Manual/waf/filter_detec/8.png){: width="800" }](/docs/images/Manual/waf/filter_detec/8.png){: target="_blank"}

<br />
## 8.날짜/시간 선택
[![image](/docs/images/Manual/waf/filter_detec/9.png){: width="800" }](/docs/images/Manual/waf/filter_detec/9.png){: target="_blank"}
- 지난 날짜와 시간을 선택하여 로그를 볼 수 있습니다.

<br />
## 9.그룹 선택
- 사용자가 등록한 시스템 그룹을 선택해서 볼 수 있습니다.

[![image](/docs/images/Manual/waf/filter_detec/10.png){: width="800" }](/docs/images/Manual/waf/filter_detec/10.png){: target="_blank"}

<br />
## 10.운영체제 선택
- 운영체제를 선택해서 볼 수 있습니다.

[![image](/docs/images/Manual/waf/filter_detec/11.png){: width="800" }](/docs/images/Manual/waf/filter_detec/11.png){: target="_blank"}

<br />
## 11.시스템 IP주소 선택
- 원하는 시스템 IP주소를 선택해서 볼 수 있습니다.

[![image](/docs/images/Manual/waf/filter_detec/12.png){: width="800" }](/docs/images/Manual/waf/filter_detec/12.png){: target="_blank"}

<br />
## 12.공격유형 선택
- 공격유형별로 선택해서 볼 수 있습니다.

[![image](/docs/images/Manual/waf/filter_detec/13.png){: width="800" }](/docs/images/Manual/waf/filter_detec/13.png){: target="_blank"}

<br />
## 13.OWASP 선택
- OWASP TOP10 에 선정된  취약점 별로 선택해서 볼 수 있습니다.

[![image](/docs/images/Manual/waf/filter_detec/14.png){: width="800" }](/docs/images/Manual/waf/filter_detec/14.png){: target="_blank"}

<br />
## 14.위험도 선택
- 위험도를 선택하여 볼 수 있습니다.

[![image](/docs/images/Manual/waf/filter_detec/15.png){: width="800" }](/docs/images/Manual/waf/filter_detec/15.png){: target="_blank"}

<br />
## 15.Status 선택
- Status 상태별 로그를 선택하여 볼 수 있습니다.

[![image](/docs/images/Manual/waf/filter_detec/16.png){: width="800" }](/docs/images/Manual/waf/filter_detec/16.png){: target="_blank"}

<br />
## 16.유형 선택
- 유형별 로그를 선택하여 볼 수 있습니다.

[![image](/docs/images/Manual/waf/filter_detec/17.png){: width="800" }](/docs/images/Manual/waf/filter_detec/17.png){: target="_blank"}

<br />
## 17.유출정보 선택
- 유출정보 유무별로 로그를 선택하여 볼 수 있습니다.

[![image](/docs/images/Manual/waf/filter_detec/18.png){: width="800" }](/docs/images/Manual/waf/filter_detec/18.png){: target="_blank"}