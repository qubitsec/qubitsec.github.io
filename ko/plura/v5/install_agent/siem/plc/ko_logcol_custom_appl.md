---
title: Custom
permalink: ko_logcol_custom_appl.html
sidebar: Install_A_S
product: Install_A_S
---

## 응용프로그램 로그 분석 – Postfix

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/YmWLsadlIdM' frameborder='0' allowfullscreen></iframe></div>

<br />

PLURA V5는 응용프로그램에 대한 로그를 업로드 설정을 이용하여 수집할 수 있습니다.

     1. 응용프로그램 원본 로그업로드를 위해서는 관리 > 목록 > 응용프로그램 태그를 등록해주어야 합니다.
     2. 수집할 경로를 파악하고 있어야 합니다.

<br />

응용프로그램 로그 업로드 설정하기[1]

[https://qubitsec.github.io/ko_set_app_log_up.html](https://qubitsec.github.io/ko_set_app_log_up.html){:target="_blank"}

<br />

## 응용프로그램 로그는 “LogStash”를 이용하여 컬럼을 분리할 수 있습니다.

Logstash는 다양한 소스로부터 데이터를 수집하고 곧바로 전환하여 원하는 대상에 전송할 수 있도록 하는 경량의 오픈 소스 서버측 데이터 처리 파이프라인입니다.

Logstash를 사용하면 시스템 로그, 웹 사이트 로그, 애플리케이션 서버 로그 등 다양한 데이터 원본에서 비정형 데이터를 쉽게 수집할 수 있습니다.[2]

<br />

## 1. Logstash 설정 방법

<br />

### 1-1. Install Logstash
[https://github.com/QubitSecurity/Logstash](https://github.com/QubitSecurity/Logstash){:target="_blank"}

<br />

### 1-2. Conf 파일 다운로드
`# cd /etc/logstash/conf.d/`

`# wget “https://raw.githubusercontent.com/QubitSecurity/Logstash/main/conf.d/70-postfix-plura.conf”`

<br />

### 1-3. Postfix 로그 경로 수정

`# vi /etc/logstash/conf.d/70-postfix-plura.conf`

[https://github.com/QubitSecurity/Logstash/blob/main/conf.d/70-postfix-plura.conf](https://github.com/QubitSecurity/Logstash/blob/main/conf.d/70-postfix-plura.conf){:target="_blank"}

[![image](/docs/images/Ins_G/LogCol_Customapp/2.png){: width="800" }](/docs/images/Ins_G/LogCol_Customapp/2.png){:target="_blank"}

`# mkdir /etc/logstash/patterns.d`

`# cd /etc/logstash/patterns.d`

`# wget “https://raw.githubusercontent.com/QubitSecurity/Logstash/main/patterns.d/grok-postfix”`

<br />

## 2. PLURA-Agent를 이용하여 업로드 설정하기

위에서 설명한 Logstash를 이용하여 Linux : Postfix 로그를 PLURA V5에서 수집해보겠습니다.

※ 테스트 환경

- 원격지 서버(자식) : CentOS Linux release 7.9.2009 (Core), Postfix, Logstash 설치

- 로그 취합서버(부모) : CentOS Linux release 7.9.2009 (Core), 라이센스 등록 및 실행

[Install Guide > SIEM > Log Collector > Application[3] : [https://qubitsec.github.io/ko_logcol_application.html](https://qubitsec.github.io/ko_logcol_application.html){:target="_blank"}

<br />

### Logstash가 설정된 원격지(자식) 서버를 등록합니다.

<br />

### 2-1. 시스템  > 시스템 관리 > 로그 취합서버(부모) 선택 > 응용프로그램 버튼을 클릭합니다.  

[![image](/docs/images/Ins_G/LogCol_Customapp/3.png){: width="800" }](/docs/images/Ins_G/LogCol_Customapp/3.png){:target="_blank"}

<br />

### 2-2. 시스템 등록 팝업 > 원격지(자식) 서버 정보를 입력합니다.
응용프로그램 사용자정의 로그 수집 경로에 “/var/log/plura/app-logstash-postfix.log”를 입력합니다.

[![image](/docs/images/Ins_G/LogCol_Customapp/4.png)](/docs/images/Ins_G/LogCol_Customapp/4.png){:target="_blank"}

<br />

### 2-3. 시스템 관리에서 경로 설정까지 완료된 후에 Logstash를 실행합니다.

RUN Logstash(foreground)

[![image](/docs/images/Ins_G/LogCol_Customapp/5.png){: width="800" }](/docs/images/Ins_G/LogCol_Customapp/5.png){:target="_blank"}

<br />

## 3. PLURA V5 웹에서 확인하기

- 경로 : 전체로그 > 응용프로그램 > 사용자정의 > postfix

※ 관리 > 사용 > 응용프로그램 > 사용자정의 설정이 ON 상태인 경우에만 메뉴가 노출됩니다.[4]

[![image](/docs/images/Ins_G/LogCol_Customapp/6.png){: width="800" }](/docs/images/Ins_G/LogCol_Customapp/6.png){:target="_blank"}

<br />

- “수정” 버튼을 클릭한 후, postfix 항목에 체크를 하면 사용자정의 응용프로그램에서 postfix로그를 확인할 수 있습니다.


[![image](/docs/images/Ins_G/LogCol_Customapp/7.png){: width="800" }](/docs/images/Ins_G/LogCol_Customapp/7.png){:target="_blank"}

<br />

Postfix 로그가 생성되면 PLURA V5 전체로그(응용프로그램)에서 확인할 수 있습니다.

[![image](/docs/images/Ins_G/LogCol_Customapp/8.png){: width="800" }](/docs/images/Ins_G/LogCol_Customapp/8.png){:target="_blank"}

<br />

## 4. 참고 사이트
[1] 응용프로그램 로그 업로드 설정하기 : [https://qubitsec.github.io/ko_set_app_log_up.html](https://qubitsec.github.io/ko_set_app_log_up.html){:target="_blank"}

[2] Logstash 정의 : [https://aws.amazon.com/ko/opensearch-service/the-elk-stack/logstash/](https://aws.amazon.com/ko/opensearch-service/the-elk-stack/logstash/){:target="_blank"}

[3] Install Guide > SIEM > Log Collector > Application : [https://qubitsec.github.io/ko_logcol_application.html](https://qubitsec.github.io/ko_logcol_application.html){:target="_blank"}

[4] Manual > Common > 관리 > 사용 : [https://qubitsec.github.io/ko_manage_use.html](https://qubitsec.github.io/ko_manage_use.html){:target="_blank"}