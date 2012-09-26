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