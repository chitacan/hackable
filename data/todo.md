# Hackable todo

다음 hackable에 반영될 item들. 반영된 item들은 삭제됨.

## Zapier

[https://zapier.com/](https://zapier.com/)

* [출처](https://plus.google.com/u/0/+xguru/posts/imghmZztevW)

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

## 카카오 링크 for android

[https://github.com/kakao/kakaolink-android] (https://github.com/kakao/kakaolink-android)

* 외부 앱, 모바일 웹에서 카카오톡 친구들에게 URL 링크 또는 메시지를 보낼 수 있는 샘플 코드
* ios, 웹 지원

## Android Patterns

[http://www.androidpatterns.com/uap_pattern/list-navigation](http://www.androidpatterns.com/uap_pattern/list-navigation)

* Android 각종 UI 패턴의 장단점 예시들을 제공해 주는 사이트
* 코드에 대한 설명은 없지만 실제로 많이 사용되는 패턴을 코드로 익혀두는 것도 괜찮을 듯

## MS 때려서 조용히 시키기 특허 출원

[http://techit.co.kr/10637](http://techit.co.kr/10637)

* 뭔가 MS 답지 않은 깨알같은 아이디어??

## Commonsware's github repo

[https://github.com/commonsguy](https://github.com/commonsguy)

* [stackoverflow](http://stackoverflow.com/users/115145/commonsware) 의 `Android` 태그 인기인인 `commonsware`의 github repo
* `Android`와 관련된 각종 예제들과 여러가지 시도들이 볼만함
* `Api Demo` 보다 쓸만한 [Busy Coder's Guide To Android Development](https://github.com/commonsguy/cw-android) 가 압권

## Next Version of Android Tools Will Allow User Created Templates

[http://www.androiduipatterns.com/2012/09/next-version-of-android-tools-will.html](http://www.androiduipatterns.com/2012/09/next-version-of-android-tools-will.html)

* 다음 버전의 ADT에는 `User created template`을 추가할 수 있는 기능이 업데이트 될 예정!!
* 벌써 공개된 [템플릿](https://github.com/jgilfelt/android-adt-templates) !?
* 이제 테스트나 앱을 만들때 자주 사용하는 패턴을 지정할 수 있게 될듯!!

## Gist.io

[http://gist.io/](http://gist.io/)

* 간단한 code snippet이나 markdown 문서를 저장하고 버전관리를 할 수 있는 [gist](http://gist.github.com) 를 활용한 재미난 웹앱
* markdown으로 작성된 gist를 불러와 웹앱의 스타일로 보여줄 수 있음
* 사용법
	* [gist](http://gist.github.com) 에 markdown 문서를 업로드
	* 해당 [gist](http://gist.github.com) 의 `ID number`를 아래와 같이 path에 추가
	
	```
http://gist.io/gist_id_number
	```
* 블로그를 통해 불특정 다수에게 공개하기는 꺼려지지만 몇몇 사람들과 글을 공유하고자 할 때 좋은 듯.
* 이놈을 수정해 hackable 뷰어를 만들어 볼 예정

## youtube-dl

[http://katselphrime.wo.tc/2012/09/29/youtube-dl/](http://katselphrime.wo.tc/2012/09/29/youtube-dl/)

* `youtube`, `vimeo` 등의 사이트에서 영상을 다운로드 받을 수 있는 콘솔 어플리케이션
* `python` 기반이라 윈도우에서도 사용가능
* 링크기반으로 자동으로 동영상을 다운로드하는 앱을 구현할 수도 있을 듯

## The GitHub hiring experience

[https://github.com/blog/1269-the-github-hiring-experience](https://github.com/blog/1269-the-github-hiring-experience)

* 요즘 가장 geek 한 회사의 geek 한 채용방법
* 채용하고자 하는 역할에 가장 알맞는 사람을 직접 찾아 컨택
	* 블로그 포스트, 이메일, 스카이프등을 통해 자기자신의 일에 얼마만큼의 이해도를 가지고 있는지 판단
	* 기본적으로 자신의 일에 관심이 있는 사람들을 대상으로 하기에, 이력서를 통한 paperwork는 생략
* 형식적인 인터뷰는 진행하지 않으며, 한번에 2명씩 10 ~ 12명의 사람들과 자유로운 분위기에서 (맥주를 마시거나 당구를 치면서) 회사의 프로세스나 지원자의 이전 일들을 공유
	* 	지원자로 하여금 회사에서 일하고 싶도록 하는 것이 목적
* 입사 첫날, [The Setup](https://speakerdeck.com/u/wfarr/p/the-setup-managing-an-army-of-laptops-with-puppet) 이란 프로그램을 통해 개발에 필요한 모든 세팅은 20분만에 완료됨.

## Vimgolf

[http://vimgolf.com/](http://vimgolf.com/)

## coursera

[https://www.coursera.org/](https://www.coursera.org/)

## Perfect Workflow in Sublime Text 2

[https://tutsplus.com/course/improve-workflow-in-sublime-text-2/](https://tutsplus.com/course/improve-workflow-in-sublime-text-2/)

	