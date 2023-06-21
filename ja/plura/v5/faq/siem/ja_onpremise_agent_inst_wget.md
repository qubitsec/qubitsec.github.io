---
title: WGETエージェントインストール
permalink: ja_onpremise_agent_inst_wget.html
sidebar: faq_siem_M_ja
topnav: topnav_ja
---

## [wget] On-premiseでPLURAエージェントインストール

### 1. CentOS 6

#### 1-1. Change Base CentOS repo

`mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.org`

`wget https://rpms.plura.io/module/baseurl/6/CentOS-Base.repo -O /etc/yum.repos.d/CentOS-Base.repo`


`mv /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6 /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6.org`

`wget https://rpms.plura.io/module/baseurl/6/RPM-GPG-KEY-CentOS-6 -O /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6`

<br />

#### 1-2. Install epel

`mv /etc/yum.repos.d/epel.repo /etc/yum.repos.d/epel.repo.org`

`wget https://rpms.plura.io/module/baseurl/6/epel.repo -O /etc/yum.repos.d/epel.repo`


`mv /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-6 /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-6.org`

`wget https://rpms.plura.io/module/baseurl/6/RPM-GPG-KEY-EPEL-6 -O /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-6`

or

`yum install https://rpms.plura.io/module/baseurl/6/epel-release-latest-6.noarch.rpm`

`mv /etc/yum.repos.d/epel.repo /etc/yum.repos.d/epel.repo.org`

`wget https://rpms.plura.io/module/baseurl/6/epel.repo -O /etc/yum.repos.d/epel.repo`

<br />

### 2. CentOS 7

#### 2-1. Change Base CentOS repo

`mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.org`

`wget https://rpms.plura.io/module/baseurl/7/CentOS-Base.repo -O /etc/yum.repos.d/CentOS-Base.repo`


`mv /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7.org`

`wget https://rpms.plura.io/module/baseurl/7/RPM-GPG-KEY-CentOS-7 -O /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7`

<br />

#### 2-2. Install epel

`mv /etc/yum.repos.d/epel.repo /etc/yum.repos.d/epel.repo.org`

`wget https://rpms.plura.io/module/baseurl/7/epel.repo -O /etc/yum.repos.d/epel.repo`


`mv /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-7 /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-7.org`

`wget https://rpms.plura.io/module/baseurl/7/RPM-GPG-KEY-EPEL-7 -O /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-7`

or

`yum install https://rpms.plura.io/module/baseurl/7/epel-release-latest-7.noarch.rpm`

`mv /etc/yum.repos.d/epel.repo /etc/yum.repos.d/epel.repo.org`

`wget https://rpms.plura.io/module/baseurl/7/epel.repo -O /etc/yum.repos.d/epel.repo`

     メーカーがサポートを終了した製品についてPLURA V5でもサポートを終了します。
     PLURA V5でサポートされていないオペレーティングシステムバージョンを使用すると、問題が発生する可能性があります。
     メーカーがサポートを終了したバージョンを使用している場合は、アップグレードについてより積極的な検討が必要です。
     ハッキングや障害など、さまざまな問題に直面し、深刻な問題に発展する可能性があるからです。