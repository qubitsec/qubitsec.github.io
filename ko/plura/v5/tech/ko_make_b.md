---
 title: Make Jekyll Blog
 permalink: ko_make_b.html
 sidebar: Tech
 topnav: topnav
---



## [vscode]

[vscode 다운로드](https://code.visualstudio.com/download)한다.

<br />

## [Git]


[Git 회원가입](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)을 진행해야 합니다.

새로운 Repository 생성

Repository 이름은 ex) username.github.io

Add a README file 체크해야 합니다. // 이유는 remote 해줘야 하기 때문입니다.

<br />

[git-scm.com](git-scm.com) 에 접속하여 Git 설치 (우측 하단 모니터 그림에 본인의 운영체제에 맞는 버전 알려줌)

[![image](/docs/images/Tech/Jekyll_Blog/Blog_1.PNG){: width="600" }](/docs/images/Tech/Jekyll_Blog/Blog_1.PNG){: target="_blank"}

[![image](/docs/images/Tech/Jekyll_Blog/Blog_2.PNG){: width="600" }](/docs/images/Tech/Jekyll_Blog/Blog_2.PNG){: target="_blank"}

[![image](/docs/images/Tech/Jekyll_Blog/Blog_3.PNG){: width="600" }](/docs/images/Tech/Jekyll_Blog/Blog_3.PNG){: target="_blank"}

**위 이미지 3개 제외하고 나머지는 기본 설정**

<br />

## [Ruby]
[https://www.ruby-lang.org/ko/](Ruby 다운로드)

[![image](/docs/images/Tech/Jekyll_Blog/Blog_4.PNG){: width="600" }](/docs/images/Tech/Jekyll_Blog/Blog_4.PNG){: target="_blank"}

들어가서 최신 버전으로 받습니다.

다 진행하면 cmd 창이 나오는데 3번 눌러준다.

<br />

## [Git 연동] cmd or VSC(terminal)

 git config –global user.name [github 계정]

 git config –global user.email [github 이메일]

 <br />

 바탕화면 폴더 생성 or 내가 저장하고 싶은 경로

 생성한 폴더로 이동 / cd 명령으로 이동
 git clone (git repository HTTPS 주소 붙여넣기)
   - 성공하면 You appear to have cloned an empty repository 메세지 나옴
   - 생성한 폴더로 가면 폴더가 하나 더 생성되어 있음.

<br />

### Git 업로드(적용)

**1. cmd**
   - git add [filename]
   - git commit -m “name(스냅샷 개념이라 본인이 하고 싶은 이름으로 설정)”
   - git push // git에 내가 올리고 싶은 파일이 올라가 있음

**2. vsc**

   - ctrl + s (저장) = 터미널에 완료 표시가 나오면 먼저 로컬 환경에서 확인할 수 있음.
   - 돋보기 아이콘 클릭
   - 넣어줄 제목 입력
   - ctrl + enter
   - sync ~~ 클릭

<br />

## [Jekyll Install]
cmd 실행

gem install jekyll

bundle install


cd C:\(~~~)
   - 자신의 블로그 폴더로 이동


jekyll new .

bundle exec jekyll serve
   - cmd에 로컬 주소 나옴(가상 환경 시작)
   
   ex) 127.0.0.1~~~
