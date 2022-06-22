---
title: Public IP주소 확인하는 방법
permalink: public_ip_check.html
sidebar: faq_common_M
topnav: topnav
---

재택 등 근무 형태 변화, 기업 외부에서 접속 가능 확대로
퍼블릭 클라우드 SaaS 서비스가 일상화된 작금의 시대에
퍼블릭 클라우드 SaaS 서비스는 자체 보안 시스템이 매우 중요합니다.

PLURA V5 웹 접속 時 보안 시스템 中 하나로
접속 IP 주소에 대한 제한을 설정할 수 있습니다.

이를 위하여는 Public IP 주소를 확인하여야 합니다.
간혹 자신이 사용하는 IP 주소와 Public IP 주소를 혼돈하는 경우가 있습니다.

많은 사용자는 집, 회사, 또는 카페와 같은 공공 장소에서 인터넷에 접속할 경우 Private (사설) IP 주소에 연결되고
인터넷으로 나갈때는 Public (공개) IP 주소로 변환됩니다.
이러한 시스템을 네트워크 주소 변환(NAT, Network Address Translation) 장비라고 불립니다.
공유기가 대표적인 NAT 장비입니다.

▶ 본인의 Public IP 주소를 확인하는 방법은 아래와 같습니다.

1. IP 주소 검색 사이트[(http://www.myipaddress.com/what-is-my-ip-address/)](http://www.myipaddress.com/what-is-my-ip-address/){: target="_blank"}에 접속합니다.

2. 본인의 IP주소를 확인하기 위해 사이트에서 **보여지는 문자를 그대로 입력**한 후, **“Show My IP Address” 버튼을 클릭**합니다.

 [![image](/docs/images/Additianal/publicIP/1.png)](/docs/images/Additianal/publicIP/1.png){: target="_blank"}

3. 본인이 사용하고 있는 IP 주소를 확인할 수 있습니다.

 [![image](/docs/images/Additianal/publicIP/2.png)](/docs/images/Additianal/publicIP/2.png){: target="_blank"}

4. 확인된 IP 주소는 PLURA V5 로그인 허용 IP주소에 추가할 수 있습니다.
▶ 상단 메뉴 중 관리 > 보안 > “로그인허용IP주소”

 [![image](/docs/images/Additianal/publicIP/3.png)](/docs/images/Additianal/publicIP/3.png){: target="_blank"}

※ 로그인 허용 IP주소 경로
※ PLURA V5 웹 로그인 > 관리 > 보안 > “로그인 허용 IP주소”

▶ PLURA V5가 제공하는 더 많은 보안 시스템 알아보기

[보안](http://blog.plura.io/?p=12969){:target="_blank"}


▶ Private (사설) IP주소 대역 확인하기

[Private IP주소 영역](http://blog.plura.io/?p=14265){:target="_blank"}