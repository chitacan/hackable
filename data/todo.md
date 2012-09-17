# Hackable todo

다음 hackable에 반영될 item들. 반영된 item들은 삭제됨.

## The UNIX System: Making Computers More Productive

[http://37signals.com/svn/posts/3249-the-unix-system-making-computers](http://37signals.com/svn/posts/3249-the-unix-system-making-computers)

* 1982년 벨 연구소에서 개발한 유닉스 시스템에 대한 소개 동영상
* 모듈, 파이프, 파일시스템, 쉘의 개념을 소개
* 저때나 지금이나 컴퓨터 앞에서 씨름하는 사람들의 자세는 똑같은 듯 ㅋ

## Zapier

[https://zapier.com/](https://zapier.com/)

* [출처](https://plus.google.com/u/0/+xguru/posts/imghmZztevW)

## 마크 주커버그의 2가지 실수

[http://techit.co.kr/10299](http://techit.co.kr/10299)

* facebook 모바일 버전의 경우 html5에 큰 베팅?
* [비판글](http://blog.creation.net/531)

## 자바 스크립트, 인기 프로그래밍 언어 랭킹 1위

[http://techit.co.kr/10392](http://techit.co.kr/10392)

* github와 stackoverflow를 기준으로 한 조사라 오픈소스 프로젝트가 많은 js가 1위를 한듯
* 실제 현업에서는 어떨지 궁금함
* Ruby가 c 형제들 (C#, C++, C) 보다 순위가 높다!!!

## prey project

[http://preyproject.com/](http://preyproject.com/)

* 노트북, 타블렛, 폰을 잃어버렸을 때 웹페이지를 통해 위치를 트래킹 할 수 있는 서비스
* [github](https://github.com/prey) 소스가 공개되어 있음
* 윈도우, 맥, 리눅스, 안드로이드, ios 클라이언트 지원

## 10 Terminal Commands That Every Mac User Should Know

[http://mac.tutsplus.com/tutorials/terminal/10-terminal-commands-that-every-mac-user-should-know/](http://mac.tutsplus.com/tutorials/terminal/10-terminal-commands-that-every-mac-user-should-know/)

* mac user 유저에게 유용한 터미널 명령어들 모음
* say 명령어를 통해 맥에게 입을 달아줄 수 있다. :)
	* 잘만 응용하면 `build complete` 같은 내용을 담아 빌드가 끝나면 음성으로 알려주는 것도 가능할 듯

## 정규표현식의 lookaround

[http://entireboy.egloos.com/4610814](http://entireboy.egloos.com/4610814)

* 매칭할 내용의 다음, 이전에 또 다른 정규식이 포함되 있는지를 매치할 때 유용하게 사용할 수 있는 RegExr
* 예를 들어 아래와 같은 2개의 user-agent가 있을 때,

```
안드로이드 디폴트 브라우저 user-agent
user-agent : mozilla/5.0 (linux; u; android 4.1.1; ko-kr; nexus s build/jro03e) appliwebkit/534.30(khtml, like gecho) version/4.0 mobile safari/534.30
```

```
안드로이드 chrome 브라우저 user-agent
user-agent : mozilla/5.0 (linux; u; android 4.1.1; ko-kr; nexus s build/jro03e) appliwebkit/534.30(khtml, like gecho) chrome/18.0.1025.166 mobile safari/535.19
```

* 이 두개의 user-agent를 구분하려면, `android` 단어 이후에 (lookahead) `chrome` 단어를 매치하는 RegExr을 만들면 된다.

```
android(?=.*chrome)
```

## Initail version for ACE editor

[http://ace.ajax.org/#nav=about](http://ace.ajax.org/#nav=about)

* javascript 기반의 웹 에디터인 ACE editor의 1.0 버전 공개.
* [cloud9 IDE](https://c9.io/)의 기본 에디터.
* 주요 특징
	* vi, emacs 키 바인딩 지원
	* 멀티 커서 에디팅
	* 자바 포함 45개 이상의 언어 syntax highlight 지원
	* html 기반의 웹 문서에 쉽게 embed 가능
* 모바일 버전은 아직 미지원