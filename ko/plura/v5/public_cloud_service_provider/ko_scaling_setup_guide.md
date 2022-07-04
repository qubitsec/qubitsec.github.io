---
title: Auto Scaling 설정 가이드
permalink: ko_scaling_setup_guide.html
sidebar: PCSP
topnav: topnav
---


## PLURA의 Amazon EC2 Auto Scaling 환경 지원

[https://qubitsec.github.io/ko_amazon_ec2_scaling.html](https://qubitsec.github.io/ko_amazon_ec2_scaling.html){:target="_blank"}

PLURA V5 에이전트가 설치된 인스턴스를 Auto Scaling 하실때 고려해야 할 사항이 있습니다.

PLURA V5는 IP주소와 호스트명을 기준으로 에이전트를 식별하며, 신규 IP주소를 갖는 새로운 Auto Scaling 인스턴스가 생성되면 PLURA V5 에이전트가 자동으로 추가/등록됩니다. 인스턴스가 종료되어도 이미 등록된 에이전트는 자동 삭제되지 않으며, 에이전트 상태만 [중지] 상태로 변경됩니다.

따라서, 인스턴스가 종료되었다가 다시 생성될 때 기존에 사용하던 IP주소가 아니라 또 다른 IP주소를 할당받는다면, 관리되는 PLURA V5 에이전트의 개수가 계속 증가하게 됩니다.

신규 인스턴스가 생성될 때, 한정된 수량 크기의 풀로부터 IP주소를 할당받도록 하면 관리되는 에이전트 목록의 크기가 불필요하게 증가하지 않도록 제한할 수 있습니다.

퍼블릭 IP주소를 미리 확보해 놓고 사용하지 않을 경우 불필요한 비용이 발생하므로, 여기서는 내부 IP주소를 할당하는 방법을 예시로 설명하겠습니다.

> 1.  고정 IP주소 확보
> 2.  에이전트 설치
> 3.  Auto Scaling 이미지 생성
> 4.  시작 템플릿 생성
> 5.  Auto Scaling 그룹 생성
> 6.  인스턴스 생성/종료 테스트

<br />

## 1. 고정 IP주소 확보

-   신규 인스턴스에 할당할 고정 IP주소 서브넷 확보  

    자동 생성되는 유동 IP주소와 충돌하지 않도록 고정IP주소 전용 서브넷을 확보합니다.  

    (인스턴스가 여러개의 가용 영역에서 생성될 경우, 각 가용 영역별로 서브넷을 만듭니다.)  

    [![image](/docs/images/Public_Cloud/autoscaling_setup/01.png)](/docs/images/Public_Cloud/autoscaling_setup/01.png){: target="_blank"}

<br />

-   고정 아이피를 지정해 놓은 네트워크 인터페이스 생성  

    Auto Scaling 최대 용량만큼 네트워크 인터페이스를 미리 생성하고, 각각에 고정IP주소를 미리 할당합니다.

    나중에 이 IP주소 목록을 user-data에 입력하게 됩니다.  

    [![image](/docs/images/Public_Cloud/autoscaling_setup/02.png)](/docs/images/Public_Cloud/autoscaling_setup/02.png){: target="_blank"}

    (Description 항목에 “plura-waf” 문자열 입력 → user-data 스크립트에서 식별자로 사용함)

<br />

## 2. 에이전트 설치

-   PLURA V5 에이전트 설치 후 다음 설정 파일에 내용을 추가합니다.  
    vi /etc/plura/conf/plura.conf
    
    > interface=eth1  
    > login_delay_sec=60
    

<br />

## 3. Auto Scaling 이미지 생성

-   에이전트가 설치된 인스턴스의 이미지를 생성합니다.  

    [![image](/docs/images/Public_Cloud/autoscaling_setup/03.png)](/docs/images/Public_Cloud/autoscaling_setup/03.png){: target="_blank"}

    [![image](/docs/images/Public_Cloud/autoscaling_setup/04.png)](/docs/images/Public_Cloud/autoscaling_setup/04.png){: target="_blank"}

<br />

## 4. 시작 템플릿 생성

-   Auto Scaling 그룹에서 사용할 시작 템플릿을 생성합니다.  

    [![image](/docs/images/Public_Cloud/autoscaling_setup/05.png)](/docs/images/Public_Cloud/autoscaling_setup/05.png){: target="_blank"}

<br />

-   시작 템플릿 콘텐츠 항목에서 이전 단계에서 생성했었던 AMI 이미지를 지정합니다.  

    [![image](/docs/images/Public_Cloud/autoscaling_setup/06.png)](/docs/images/Public_Cloud/autoscaling_setup/06.png){: target="_blank"}

<br />

-   고급 세부 정보 > 사용자 데이터 항목에 고정IP주소 및 호스트명 할당 스크립트를 입력합니다.  

    [![image](/docs/images/Public_Cloud/autoscaling_setup/07.png)](/docs/images/Public_Cloud/autoscaling_setup/07.png){: target="_blank"}

<br />

-   고정IP주소 및 호스트명 할당 스크립트는 아래를 참조하세요.  

    (환경에 맞게 접근키, 비밀키, IP주소 값을 수정합니다.)  

    [![image](/docs/images/Public_Cloud/autoscaling_setup/08.png)](/docs/images/Public_Cloud/autoscaling_setup/08.png){: target="_blank"}

<br />

## 5. Auto Scaling 그룹 생성

-   Auto Scaling 그룹을 생성하고, 이전 단계에서 만들어 놓은 시작 템플릿을 지정합니다.  

    [![image](/docs/images/Public_Cloud/autoscaling_setup/09.png)](/docs/images/Public_Cloud/autoscaling_setup/09.png){: target="_blank"}

    [![image](/docs/images/Public_Cloud/autoscaling_setup/10.png)](/docs/images/Public_Cloud/autoscaling_setup/10.png){: target="_blank"}

<br />

## 6. 인스턴스 생성/종료 테스트

-   Auto Scaling 그룹 > 세부 정보 탭 > 그룹 세부 정보 [편집] 눌러서 그룹 크기 조정  

    [![image](/docs/images/Public_Cloud/autoscaling_setup/11.png)](/docs/images/Public_Cloud/autoscaling_setup/11.png){: target="_blank"}

<br />

-   원하는 용량 항목에 값을 지정하여 수동으로 인스턴스의 개수를 변경할 수 있습니다.  

    [![image](/docs/images/Public_Cloud/autoscaling_setup/12.png)](/docs/images/Public_Cloud/autoscaling_setup/12.png){: target="_blank"}

<br />

-   PLURA V5 페이지의 시스템 > 시스템관리에서 에이전트 목록을 확인  

    [![image](/docs/images/Public_Cloud/autoscaling_setup/13.png)](/docs/images/Public_Cloud/autoscaling_setup/13.png){: target="_blank"}

<br />
    
-   새로운 IP주소 및 호스트명으로 신규 인스턴스가 생성되면 에이전트가 자동으로 추가됩니다.  

    이후 인스턴스가 종료되어도 에이전트는 삭제되지 않고, 단지 동작 상태만 [중지]로 변경됩니다.  

    (아이콘 상태가 변경되기 까지는 최대 5분 소요)  

    [![image](/docs/images/Public_Cloud/autoscaling_setup/14.png)](/docs/images/Public_Cloud/autoscaling_setup/14.png){: target="_blank"}

<br />

-   새로 생성된 인스턴스가 이미 등록된 에이전트의 IP주소/ 호스트명과 같다면, 시스템관리 화면에 에이전트가 새로 추가되는 대신 상태만 변경될 것 입니다.  

    (아이콘 상태 즉시 변경)