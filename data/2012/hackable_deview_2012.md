# Hackable
deview 2012 feature.

## 키노트

* 김동욱 NHN 포털 센터장의 키노트는 재미는 있었지만 약간은 산만한 진행으로 아쉬웠음
* 하지만 `{()(){(){}}}` 같은 것들을 보여주며, 개발자들만이 알 수 있는 깨알같은 개그 요소들이 있었음
* 가장 마음에 와 닿은 이야기는
	* UX는 사용자의 행동 패턴을 바꾸는 것이 아니라
	* 사용자의 행동 속으로 들어가서 그 속에 자연스럽게 서비스를 놓아두는 것
* 두번째 키노트는 `world is flat` 이란 단어 말고는 생각이 나지 않음

## 루비는 패셔니스타

[http://deview.kr/2012/xe/index.php?mid=track&document_srl=391&time_srl=233](http://deview.kr/2012/xe/index.php?mid=track&document_srl=391&time_srl=233)

* `A 트랙`의 첫번째 세션. 사실 이번 deview는 `node.js` 세션 하나만 보고 간 것이라 나머지 세션들은 가볍게 들어보려 했는데 의외의 수확을 얻었던 세션
* `루비`의 창시자 아저씨의 목표는 

	```
	펄보다 강력하고 파이선보다 객체지향적인 언어
	무엇보다도 재미있는 코딩을 추구
	인간 지향적인 언어 설계
	```

* 한국에서는 `스프링` + `기타등등`등에 의해 거의 왕따 취급을 당하지만, 외국에서는 이미 성숙한 언어로 대우받고 있으며 여러 유명 프로젝트들이 루비에서 영감을 얻거나 루비 언어를 사용함.
	* `underscore`, `coffee script`, `homebrew` 등등
* `레일즈` 역시 외국에서는 `github`, `twitter`등의 성공사례가 많지만, 우리나라에서는 거의 없음
	* 느리다는 이유 하나로 한국에서 도입 초기부터 외면받음
	* 하지만 `레일즈`의 빠른 생산성은 스타트업에겐 충분히 매력적인 플랫폼
* `루비`를 왜 배워야 하는가?
	* 매년 새로운 언어를 배워라
		* 다른 언어들은 똑같은 문제를 다르게 풀기 때문에.
	* 내가 사용하고 있는 언어의 한계가 내 실력의 한계다.
	
## Android Security의 과거와 미래

[http://deview.kr/2012/xe/index.php?mid=track&document_srl=442&time_srl=244](http://deview.kr/2012/xe/index.php?mid=track&document_srl=442&time_srl=244)

* T-Store 보안 담당자로 부터 안드로이드 보안의 히스토리에 대해 짧게나마 배울 수 있었던 세션
* 안드로이드 앱은 `구글의 가이드를 따른 리눅스 앱`
	* 기존의 리눅스 프로세스에 `jni`, `package manager`, `activity manager`, `android manifest`, `dvm`등을 추가한 것일 뿐
	* 결국 앱 내에서는 기존 리눅스 프로세스에서 하던 일들을 다 해도 상관없다. 다만 본인의 앱에 대해서는 본인이 책임을 져야 할 뿐…
	* unity 3D는 `dvm`이 아닌 요상한 `vm`을 자체 제작해 띄우기까지 한다;;;
* 안드로이드의 보안 기능들
	* memory protection
		* 2.3+ 부터 힙과 스택에서는 코드가 실행 불가능하도록 수정
		* 기존엔 2.3 이전엔 boot process를 빠르게 하기 위해 so파일이 로드되는 메모리 주소가 노출되어 있었지만 이제는 사용되지 않음
	* PIE(position independant excutable) : 프로세스가 실행될 때마다 실행되는 메모리 주소가 달라짐
	* file system encryption 지원
	* credential storage 지원
* 안드로이드의 copy protection 히스토리
	* protected APK
		* dex 파일을 `/data/app`이외에 `/data/app-private`에 놔두던 기능
		* 루팅되면 말짱 도루묵
	* LVL (License Verification Library)
		* 디컴파일 or 코드를 직접까서 LVL을 확인하는 곳을 bypass 해버리면 끝…
	* encrypted APK
		* 젤리빈 부터 지원하는 나름 최신 copy protection
		* APK 자체를 암호화
		* 하지만 발표자는 APK 실행을 위해 런처가 읽을 수 있는 권한의 파일이 생성될 것이고 이를 통해 뚫릴 것이라고 예상함
* odex file
	* `dvm`은 pre-installed apk의 `dex`를 가지고 `odex`를 만들어 `dalvik-cache`와 같은 디렉토리에 떨궈놓음
	* 하지만 `odex`역시 리버싱이 가능하기에 pre-installed 된 앱들도 코드가 유출됨
	* 4.0+ 부터는 `odex` 파일을 떨구지 않고 메모리상에서 `odex`를 맏들 수 있는 기능이 추가됨
* SE Android
	* SELinux(NSA에서 만든 리눅스??)를 AOSP (android open source project)에 적용한 것
	* 이미 머지가 되어 있는데, 어디에 어떻게 사용할 지는 미지수
		* external/libselinux, external/sepolicy, core/java/SELinux.java, core/jni/AndroidRuntime.cpp
* 그럼 개발자들은 어떻게 자신의 APK를 보호해야 하나?
	* 난독화는 필수
	* 정말 중요한 코드들은 네이티브로
	* 데이터는 반드시 서버에 저장
		* 인 앱 빌링도 로컬에 데이터가 있다면 뚫을 수 있다.
	* 개발자의 창의력을 발휘해야 할 시간 ㅠ
	
## Collie - HTML5를 이용해 자바스크립트 애니메이션과 게임을 만들 수 있는 오픈소스 라이브러리

[http://deview.kr/2012/xe/index.php?mid=track&document_srl=395&time_srl=253](http://deview.kr/2012/xe/index.php?mid=track&document_srl=395&time_srl=253)

* 애니메이션의 기초와 `collie` 라이브러리에 대한 소개 & 성능에 관한 세션
* 각종 모바일 단말에서의 자바스크립트 애니메이션 구현을 위한 팁들을 얻을 수 있었음
* `collie`는
	* 18 종 이상의 모바일 기기(android + ios)에 대응하는 모바일에 최적화된 자바스크립트 라이브러리
	* 최적화를 통해 기존의 애니메이션보다 더 빠른 방식으로 렌더링
	* 정밀한 이벤트 영역 탐색을 위한 hitArea 사용가능
	* 비동기 이미지 처리
	* 레티나 디스플레이지원
	
	등등이 된다고 자랑함;;
	
## 3G 네트워크에 대한 이야기 +a

[http://deview.kr/2012/xe/index.php?mid=track&document_srl=397&time_srl=260](http://deview.kr/2012/xe/index.php?mid=track&document_srl=397&time_srl=260)

* 제목에서 부터 [3G 모바일 네트워크 이해](http://helloworld.naver.com/helloworld/111111)의 확장판인 듯한 기운이;;
* 3G 네트워크 성능 측정을 하면서 얻게된 정보들에 대해 공유하기 위한 세션
* LTE가 대세인데 왜 굳이 3G 네트워크 성능을 측정??
	* 아직 LTE 사용자수는 3G사용자 수의 1/3
	* 네이버 모바일 페이지의 PV(page view)역시 3G가 LTE의 2배
	* 3G가 글로벌 로밍에 유리하기에 
* 3G 네트워크의 구조, 특징
	* 크게보면 ip 패킷이 이통사의 거대한 VPN을 통해 전닫되는 구조
	* 안테나 바가 다 차 있어도 (시그널은 좋은 상태여도) 이통사 VPN 내부의 패킷 스케쥴링 정책에 의해 패킷 전달이 오래 걸릴 수 있음
* 실제 모바일 환경에서는 bandwidth 보다 latency가 속도에 더 많은 영향을 미침
* 단말, m.naver.com 서버간의 RTT(round trip time)을 측정해 보면
	* 3g의 경우 대략 100ms
	* 여기에 tcp 3way handshaking을 위해 3번 왕복 + dns 쿼리 + redirection이 되면서 RTT는 5배에서 6배까지 증가.
	* 거기에 3G의 RRC protocol 영향까지 겹치면 ...
		* RRC protocol : 무선채널을 효율적으로 사용해 cell 당 동접을 최대화 하기 위한 기법으로, 기본적으로 기지국은 일정시간 동안 네트워크를 사용하지 않은 단말에 대해 연결을 해제하고 3G 모뎀을 sleep 상태로 돌리도록 한다. 3G 모뎀이 sleep 상태에서 통신 가능한 상태로 돌아오기 위해서도 시간이 걸린다.
	* 설상가상으로 TCP flow control에 의해 패킷을 나눠 보내는 과정에서 RTT 횟수가 늘어 날 수 있다.
		* 이는 서버단에서 congetion window를 조절함으로써 극복 할 수 있다.
* 효율적이고 빠른 3G 네트워크를 위해서는
	* 데이토 통신은 한번에 몰아서 한방에 끝내는 것이 좋다.
	* 한방에 끝내는 데이터의 양도 최소화
	* 앱과 서비스의 특성에 맞게 통신패턴을 최대한 조작(TCP flow control)

## node.js를 이용한 단일언어 기반 웹 애플리케이션 개발

[http://deview.kr/2012/xe/index.php?mid=track&document_srl=417&time_srl=267](http://deview.kr/2012/xe/index.php?mid=track&document_srl=417&time_srl=267)

* 이번 deview의 목표 세션. 제일 큰 강의장인 c 트랙이 거의 꽉 찰 정도로 많은 분들이 오심
* 발표자는 웹페이지 몇개 만들기위해 무수한 기술을 배워야 하는 `스프링`, `톰캣`에 대한 대안으로 `node.js`를 소개
* 실제로 발표에 주제인 [devnote](https://github.com/nforge/devnote)의 경우, 서버 & 클라이언트 코드 뿐만 아니라 테스트 코드, config 파일 심지어는 make 파일까지 자바스크립트로 구현되어 있음
* `devnote` 개발의 목표
	* 삽질 비용을 먼저 치루고 그 결과를 공유 / 공개
	* 우리나라 웹 개발에 `spring`, `jsp` 말고 딴걸 쓰고 싶었다는 ㅋㅋ
* `devnote`에 사용된 오픈소스 프로젝트들과 결정배경에 대한 소개
* 오픈소스 도입의 단점 극복방법 소개
	* 비슷한 모듈들을 너무 많은데, 어떻게 결정?
	* 정확히 원하는 기능이 없을 수 있음
	* 발전을 기대하기 보다는 현재의 기능에서 우리에게 가장 맞는 것을 선택하는 것이 핵심
	* 최악을 가정한 의사결정도 필요함
* nodejs korea conference에 대한 이야기도
	* 실제 node.js의 커미터들이 방한 예정
	* 날짜는 11/20

## Deview 2012 반응형 웹 구축기

[http://deview.kr/2012/xe/index.php?mid=track&document_srl=389&time_srl=274](http://deview.kr/2012/xe/index.php?mid=track&document_srl=389&time_srl=274)

* [이 세션](http://deview.kr/2012/xe/index.php?mid=track&document_srl=1423742&time_srl=275) 이랑 둘중에 고민을 많이하다 선택했는데 조금 아쉬웠음
* 실제 사이트의 코드를 보여줄 줄 알았는데, 기본적인 개념들에 대한 설명이 주
* 반응형 웹 구축에 필요한 html 속성과 CSS 문법을 설명

	