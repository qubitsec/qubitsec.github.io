---
title: 사용
permalink: manage_use.html
sidebar: M_C
topnav: topnav
---

- 사용 : 데이터 유출 설정, 웹 개인 정보 숨김, 웹 탐지 예외 설정, 웹/시스템/응용프로그램/네트워크 업로드 설정을 할 수 있습니다.

※ PLURA V5 Forensic 제품에서는 데이터 유출 설정, 웹/시스템 업로드 설정 기능을 지원하지 않습니다.

[![image](/docs/images/Manual/common/manage/use/1.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />
웹 개인정보 숨김 : 웹로그 사용 시 개인정보 숨김 설정이 가능하며 설정하면 해당 정보를 *로 표시합니다.

**예시) pwd에 대한 값을 숨김 설정하기**

아래와 같이 pwd 값이 그대로 노출되고 있는 웹로그를 예로 들어 숨김 설정을 해보도록 하겠습니다.

[![image](/docs/images/Manual/common/manage/use/2.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />
### 1.관리 > 사용 > 웹 개인정보숨김 > 설정 버튼을 클릭합니다.

[![image](/docs/images/Manual/common/manage/use/3.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />
### 2.숨기고자 하는 개인정보를 추가합니다.

[![image](/docs/images/Manual/common/manage/use/4.png)](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />
### 3.개인정보 숨김 설정이 정상적으로 적용된 것을 확인할 수 있습니다.

[![image](/docs/images/Manual/common/manage/use/5.png)](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

 - 웹탐지예외 : 전체로그에는 올라오지만 탐지로그에는 올라오지 않도록 설정할 수 있습니다.

예시) host 주소가 123.34.45.1 인 로그는 탐지가 안되도록 설정 하고 싶으면 host 선택 후 123.34.45.1 을 기입하면 됩니다.

   - 관리 > 사용 > 웹탐지예외 > 예외설정 추가 선택

[![image](/docs/images/Manual/common/manage/use/6.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}
 
<br />
   - 그룹에서 +로 추가하는 항목들은 AND 조건, 그룹 간에는 OR 조건입니다.

[![image](/docs/images/Manual/common/manage/use/7.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />
- 웹 업로드 : 사용자가 원하는 웹 업로드 형식을 선별 또는 예외처리할  수 있습니다.
웹 업로드 설정의 경우, 기본적인 이미지 등의 디폴트 설정이 되어있으며 사용자에 의해 수정이 가능합니다.

[![image](/docs/images/Manual/common/manage/use/8.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />
※ [참고] 웹 업로드 Default 설정값

▶ Extension : (?i)^(jpg|gif|png|jpeg|ico|bmp|tiff|exif|ppm|pgm|pbm|
pnm|mng|pgf|tga|bpg|cgm|svg|hevc|wmv|Xvid|VP6|VP7|VP8|VP9|MPEG-1|
MPEF-2|MPEF-4|ACC|mp4|avi|asf|wav|otf|woff|woff2|eot|ttf|less|js|css)$

▶ Req-Content Type : (?i)(image|video|audio|font)

   - 시스템 업로드 : 사용자가 원하는 시스템 업로드 형식을 OS 별로 선별 또는 예외처리할 수 있습니다.

<br />
[![image](/docs/images/Manual/common/manage/use/9.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />
**[윈도우 에이전트]** 이벤트 채널에 대한 로그 수집을 ON/OFF 할 수 있습니다.

※ 설정 OFF인 경우, 해당 채널에 대한 로그 수집을 하지 않습니다.

경로 : C:\ → Program Files(x86) → PLURA → 메모장(또는 Notepad++)에서 @ELC_config.ini 파일 실행(관리자 권한)

[![image](/docs/images/Manual/common/manage/use/10.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />
@ELC_config.ini 파일을 관리자 권한으로 실행한 후, 아래의 설정값을 추가합니다.
- on(채널 로그 수집 활성화), off(채널 로그 수집 비활성화)

     [EVENTLOG]

     DEFAULT=off
     SECURITY=off
     ETC=on

<br />
- DEFAULT Channel : Application, System, Setup, Sysmon log
- SECURITY Channel : Security log
- ETC : DEFAULT, SECURITY Channel 로그를 제외한 모든 로그

[![image](/docs/images/Manual/common/manage/use/11.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}
 
<br />
- 응용프로그램 원본 업로드 : 사용자가 원하는 응용프로그램 로그를 선별/예외처리할 수 있습니다.

[![image](/docs/images/Manual/common/manage/use/12.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

- 응용프로그램 업로드 → 공백 예외
  원본 로그 중 공백을 예외하고 싶은 경우

{ “timegenerated”: “2022-05-21T13:20:45.098193+09:00”, “tag”: “top”, “path”: “/var/log/pluraagent.txt”, “msg”: “” }

1. 공백이 1회 이상일때는 > ^\s+$

2. 공백이 0회 이상일때는 > ^\s*$

<br />
예시 이미지)

[![image](/docs/images/Manual/common/manage/use/13.png)](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />
- 응용프로그램 사용자 정의 : 노출하고 싶은 사용자 정의 항목을 설정합니다.
※ 선택한 항목만 대시보드, 전체로그, 필터탐지, 보고서 메뉴에서 노출됩니다.

[![image](/docs/images/Manual/common/manage/use/14.png)](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

<br />
- 네트워크 업로드 : 사용자가 원하는 네트워크 로그를 선별/예외처리할 수 있습니다.

[![image](/docs/images/Manual/common/manage/use/15.png){: width="800" }](/docs/images/Manual/common/manage/use/1.png){: target="_blank"}

[관련 블로그]

- Video > 기능소개 > SIEM > 업로드설정 DEMO : [https://qubitsec.github.io/upload_setting.html](https://qubitsec.github.io/upload_setting.html){: target="_blank"}