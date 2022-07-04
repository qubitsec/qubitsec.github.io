---
title: CURL 에이전트 설치하기
permalink: ko_onpremise_agent_curl.html
sidebar: faq_siem_M
topnav: topnav
---

     On-premise 에서 PLURA 에이전트 설치하기 curl

## 1. CentOS 6

### 1-1. Change Base CentOS repo

`mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.org`

`curl -o /etc/yum.repos.d/CentOS-Base.repo https://rpms.plura.io/module/baseurl/6/CentOS-Base.repo`


`mv /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6 /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6.org`

`curl -o /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6 https://rpms.plura.io/module/baseurl/6/RPM-GPG-KEY-CentOS-6`

<br />

### 2-2. Install epel

`mv /etc/yum.repos.d/epel.repo /etc/yum.repos.d/epel.repo.org`

`curl -o /etc/yum.repos.d/epel.repo https://rpms.plura.io/module/baseurl/6/epel.repo`


`mv /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-6 /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-6.org`

`curl -o /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-6 https://rpms.plura.io/module/baseurl/6/RPM-GPG-KEY-EPEL-6`

or

`yum install https://rpms.plura.io/module/baseurl/6/epel-release-latest-6.noarch.rpm`

`mv /etc/yum.repos.d/epel.repo /etc/yum.repos.d/epel.repo.org`

`curl -o /etc/yum.repos.d/epel.repo https://rpms.plura.io/module/baseurl/6/epel.repo`

<br />

## 2. CentOS 7

### 2-1. Change Base CentOS repo

`mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.org`

`curl -o /etc/yum.repos.d/CentOS-Base.repo https://rpms.plura.io/module/baseurl/7/CentOS-Base.repo`


`mv /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7.org`

`curl -o /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 https://rpms.plura.io/module/baseurl/7/RPM-GPG-KEY-CentOS-7`

<br />

### 2-2. Install epel

`mv /etc/yum.repos.d/epel.repo /etc/yum.repos.d/epel.repo.org`

`curl -o /etc/yum.repos.d/epel.repo https://rpms.plura.io/module/baseurl/7/epel.repo`


`mv /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-7 /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-7.org`

`curl -o /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-7 https://rpms.plura.io/module/baseurl/7/RPM-GPG-KEY-EPEL-7`

or

`yum install https://rpms.plura.io/module/baseurl/7/epel-release-latest-7.noarch.rpm`

`mv /etc/yum.repos.d/epel.repo /etc/yum.repos.d/epel.repo.org`

`curl -o /etc/yum.repos.d/epel.repo https://rpms.plura.io/module/baseurl/7/epel.repo`

     제조사가 지원을 종료한 제품에 대하여 PLURA V5에서도 지원을 종료합니다.
     PLURA V5에서 지원하지 않는 운영체제 버전을 사용한다면 문제가 발생할 수 있습니다.
     제조사가 지원 종료한 버전을 사용 중이라면 업그레이드에 대하여 보다 적극적인 검토가 필요합니다. 해킹과 장애 등 다양한 문제에 직면하고 심각한 문제로 발전할 수 있기 때문입니다.