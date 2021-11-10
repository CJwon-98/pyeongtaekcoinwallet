# 할 것
- 윈도우에서 안드로이드 앱 동작 방법 찾아보기 (e.g. qt)
- 네트워크 연결문제 해결 (팀즈 `팀 > PC Client Team > 파일 > Document > olivingcoin pc client`에 문서 있음)
```
- 네트워크 연결 순서: 앱 > Menu > Settings > Advanced Settings > Pyeongtaekcoin Nodes
- 접속하고 기다리면 팅기는 문제 발생
- 관련 코드 보기
- 기본 설정값 변경 하기: IP연결 192.168.0.17 (포트는 기본값)
- PC클라이언트 다운받아서 테스트 해보기
```
- kiosk에서 사용자의 결제 구분하는 방법 생각하기 (e.g. tx에 특정 메세지 전송)
- web에서 `menu_coffee.html` 페이지 갈 수 있게 연결하기
- 수요일에 `menu_coffee.html`에서 커피 아이템누르면 주문 리스트로 가게 javascript작성하기

# 한 것
## 2021-07-29
- kiosk java 클래스 틀 제작

## 2021-07-30
- 전체회의
- 먼저 키오스크 동작 만들고 나서 네트워크 관련 문제 해결

## 2021-08-09
- 레이아웃, 액티비티 작성
- QR모듈 알아보기
- 두 프로젝트(`loafwallet-android`, `loafwallet-android-kiosk`) `코인 이름 / APK 이름` 다시 `oliving -> lite`으로 바꾸기 (git revert 이용해서 예전에 커밋 기록 되돌림)

## 2021-08-11
- Github에 push 자주하기
- 서로 같은 파일 수정 금지
- QR은 내부 QR 모듈 사용을 우선으로 개발 

## 2021-08-12
```yml
# 해결한 문제점
## kiosk 새로운 AVD 만들어서 하면 멈춤(paper key 안 만들어짐)
- paper key 만든 후에 앱이 백그라운드에서 돌아가는 동작이 있는데, kiosk lock이 
안드로이드 버전10 이상부터 백그라운드 동작을 막아서 앱이 중간에 종료됨
- 그래서 paper key만들고 나서 BreadActivity가 실행되면 바로 MainActivity(kiosk lock 화면)
로 넘어가게 해서 kiosk mode를 나중에 실행하도록 변경

## 화면 전환 처리 
- AndroidManifest.xml에 loafwallet-android의 기본 activity인 IntroActivity가 등록이 안되있었음
```
- AndroidManifest.xml에서 시작 activity 변경: `MainActivity(kiosk)` > `IntroActivity(기본)`
> activity 흐름: `IntroActivity` > `MainActivity` > `OrderMethodActivity`
- Order관련 activity 의 컴포넌트 클래스 타입 xml과 맞춤
- BreadActivity에서 onCreate()에다가 바로 MainActivity실행하게 변경

## 2021-08-17
- OrderMenuActivity의 ListView와 Adapter 관련 수정 [참고](http://i5on9i.blogspot.com/2012/11/listview-getview.html), [참고](https://baessi.tistory.com/52)

## 2021-08-20
- OrderMenuActivity화면에서 QRRequestFragment 창 띄우기 성공
- Lock 해제 기능 추가: `OrderMethodActivity`화면에서 `뒤로가기` 버튼 길게 누르기 (계속 뒤로 가기 눌러서 `EndLock` 눌러도 됨)

## 2021-08-23
- 메뉴화면의 ListView(Adapter) 버그 수정
- 키오스크 LOCK 개발동안 잠시 사용 안하기 (Setting에서 변경 가능) (이유: 개발 속도 높이기 위해)
- OrderMenuActivity와 QRPay 연결

## 2021-08-24
- QR pay결제 동작 Order와 연결 (FragmentRequestAmount객체를 불러올 수 없어서 일단 간단한 방식으로 해결)
```yml
- address: Setting.ADDRESS 사용
- amount: QRPay.getTotalPrice() 사용
- 키보드 삭제
```

## 2021-08-25
- 키오스크 기본 기능(레이아웃, 액티비티, QR모듈) 완성

## 2021-11-01
- 유저의 결제 구분 방법: request에서 `label`, `message` 같은 요소를 활용하면 구분 할 수도 있어보임, 일단은 결제 주소를 랜덤으로 생성하고, 결제가 이뤄지면 한 서버에서만 
장부에 올라온 결제들의 output주소(가상주소)를 확인하고 결제된 페이지들에게 결제 완료 뜨게 하기 (임시방편)
- sync가 안되어도 거래만 서로 결제가 되면 그것을 이용해서 결제 확인하게 하기 (임시방편) (만약 이것도 안되면 app에서 지갑 생성될 때 기본적으로 금액을 주기)

## 2021-11-09
- web에서 메뉴 아이템 변경되게 수정
- web에서 결제시 QR이미지 불러옴








