# Hackable
40

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

* 이 두개의 user-agent중 chrome 브라우저를 선택하려면, `android` 단어 이후에 (lookahead) `chrome` 단어를 매치하는 아래와 같은 RegExr을 만들면 된다.

	```
android(?=.+chrome)
	```

## 카카오 링크 for android

[https://github.com/kakao/kakaolink-android] (https://github.com/kakao/kakaolink-android)

* 외부 앱, 모바일 웹에서 카카오톡 친구들에게 URL 링크 또는 메시지를 보낼 수 있는 샘플 코드
* ios, 웹도 지원

## Commonsware's github repo

[https://github.com/commonsguy](https://github.com/commonsguy)

* [stackoverflow](http://stackoverflow.com/users/115145/commonsware) 의 `Android` 태그 인기인인 `commonsware`의 github repo
* `Android`와 관련된 각종 예제들과 여러가지 시도들이 볼만함
* `Api Demo` 보다 쓸만한 [Busy Coder's Guide To Android Development](https://github.com/commonsguy/cw-android) 가 압권

## Zapier

[https://zapier.com/](https://zapier.com/)

* [출처](https://plus.google.com/u/0/+xguru/posts/imghmZztevW)
* 106개에 달하는 다양한 웹 서비스 API들을 드래그 & 드랍으로 연결시켜 볼 수 있는 서비스
* 각 서비스들의 모든 API를 사용할 수는 없지만 연결 가능한 API들로도 충분히 재미있는 시도를 해 볼 수 있을 듯.
	* `GitHub`와 `google calendar`를 연결해 `pull request`가 오면  코드리뷰 일정을 잡거나,
	* `Dropbox`와 `Twitter`를 연결해 특정 새 파일이 올라오면 링크를 트위터로 전송하는 등의 응용이 가능.
* 우리에게 친숙한 서비스들이 없다는 것이 흠이라면 흠.

## deview 2012 다시보기 서비스 오픈

* [deview 2012](http://deview.kr/2012/xe/index.php) 의 세션을 온라인에서 볼 수 있는 서비스 오픈
* **Track F, G 를 제외한** 나머지 트랙 세선들의 다시보기 가능
* 추천 세션은 (개인적인 기준 ㅋ)
	* [루비는 패셔니스타](http://deview.kr/2012/xe/index.php?mid=track&document_srl=391&time_srl=233)
	* [Android Security의 과거와 미래](http://deview.kr/2012/xe/index.php?mid=track&document_srl=442&time_srl=244)
	* [Beyond Android Binder](http://deview.kr/2012/xe/index.php?mid=track&document_srl=444&time_srl=251)
	* [3G 네트워크에 대한 이야기 +a](http://deview.kr/2012/xe/index.php?mid=track&document_srl=397&time_srl=260)
	* [node.js를 이용한 단일언어 기반 웹 애플리케이션 개발](http://deview.kr/2012/xe/index.php?mid=track&document_srl=417&time_srl=267)
	* [Creating an attractive platform](http://deview.kr/2012/xe/index.php?mid=track&document_srl=1423742&time_srl=275)