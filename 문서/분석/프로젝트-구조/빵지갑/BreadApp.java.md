# BreadApp 클래스 역할 및 특징

### 참고
`함수의 역할이 정확한지는 잘 모르겠음.`

## 역할
- Activity의 생명주기와 관련됨

## 특징
- Application 클래스를 상속 받음


* * *

# 변수 역할

- DISPLAY_HEIGHT_PX: 디스플레이 높이 픽셀
- HOST: ip를 가지고 있고 양방향 통신이 가능한 컴퓨터("api.loafwallet.org")
- isBackgroundChecker: 배경 확인?
- backgroundedTime: 배경시간?

- currentActivity: (private타입) 현재 사용자와 상호작용을 담당하는 인터페이스



* * *

# 메소드 역할

## onCreate()  
- 활동의 전체 수명 주기 동안 한 번만 발생해야 하는 기본 애플리케이션 시작 로직을 실행. 
- 액티비티가 생성될 때 호출되며 사용자 인터페이스 초기화에 사용됨.
- [참고 링크](https://developer.android.com/guide/components/activities/activity-lifecycle?hl=ko)
- [참고 링크](https://velog.io/@jojo_devstory/%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-%EC%95%A1%ED%8B%B0%EB%B9%84%ED%8B%B0-%EC%83%9D%EB%AA%85%EC%A3%BC%EA%B8%B0LifeCycle-%EB%B0%8F-%EC%A0%84%EA%B3%B5%EC%9E%90%EB%8F%84-%EC%9E%90%EC%A3%BC-%ED%8B%80%EB%A6%AC%EB%8A%94-%EC%83%9D%EB%AA%85%EC%A3%BC%EA%B8%B0-%EC%88%9C%EC%84%9C)

- 오버라이딩(재구현함)
- (참고)크래시리틱스(Crasshlytics): 앱에서 충돌이 일어날 때 무엇이 문제인지 알아내는 것이 중요한데 크래시리틱스는 충돌을 찾아내서 어떤 코드가 문제를 일으키는지 찾아줌
- 포인트 사이즈 객체 생성
- 디스플레이 사이즈를 함수로 갖고 옴
- size.y의 값을 DISPLAY_HEIGHT_PX에 저장 




## getBreadContext()
- currentActivity(현재활동)이 NULL이면 SyncReceiver.app, NULL이 아니면 currentActivity을 리턴함.
- SyncReceiver.app: 
- 안드로이드에서는 Context가 있어야 리소스나 클래스에 접근하거나, 안드로이드의 4대 컴포넌트등을 시작할 수 있다.
출처: https://karrel.tistory.com/37 [카렐님의 프로그래밍]
- [참고 링크](https://karrel.tistory.com/37)



## setBreadContext(Activity app)
- app값을 currentActivity에 저장(currentActivity = app)




## fireListeners()
- if문(listeners가 null이면 리턴)
- listeners: 특정 이벤트를 처리하는 인터페이스. 사용자가 어떤 액션을 취할 때마다(버튼 클릭, 키보드 키 입력 등) 메시지가 발생해서 해당 메시지의 핸들러가 미리 정의해둔 행동을 하는 것이 안드로이드의 리스너
- for (OnAppBackgrounded lis : listeners) lis.onBackgrounded();




## addOnBackgroundedListener(OnAppBackgrounded listener)
- listeners가 없으면 listeners = new ArrayList<>()를 생성(배열 리스트를 생성)
- listeners가 포함 안되어 있으면 listeners를 포함한다. (listeners.add(listener);)




## isAppInBackground(final Context context)
- Context클래스의 context가 null이거나(or) activityCounter.get() <= 0이면 리턴




## onStop(final BRActivity app)
-  활동이 사용자에게 더 이상 표시되지 않으면 중단됨 상태에 들어가고, 시스템은 onStop() 콜백을 호출함.
- 사용자가 멀티 윈도우 모드에서 활동을 보고 있더라도 UI 관련 작업이 계속 진행됨.
- 액티비티가 더이상 사용자에게 보여지지 않을 때 호출됨. 메모리가 부족할 경우에는 onStop() 메소드가 호출되지 않을 수도 있음.
- [참고 설명](https://developer.android.com/guide/components/activities/activity-lifecycle?hl=ko)
- [참고 링크](https://velog.io/@jojo_devstory/%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-%EC%95%A1%ED%8B%B0%EB%B9%84%ED%8B%B0-%EC%83%9D%EB%AA%85%EC%A3%BC%EA%B8%B0LifeCycle-%EB%B0%8F-%EC%A0%84%EA%B3%B5%EC%9E%90%EB%8F%84-%EC%9E%90%EC%A3%BC-%ED%8B%80%EB%A6%AC%EB%8A%94-%EC%83%9D%EB%AA%85%EC%A3%BC%EA%B8%B0-%EC%88%9C%EC%84%9C)




## run() 
- onStop()내에 있음, 오버라이딩함(재구현)
- 스레드를 생성할 때:스레드를 통해 작업하고 싶은 내용을 run() 메소드에 작성함




## OnAppBackgrounded 
- void onBackgrounded()을 실행시킴




## CrashReportingTree
- 오류 보고를 하는 클래스
- priority(우선권), 

## log(int priority, String tag, String message, Throwable throwable)
- CrashReportingTree 클래스 내에 들어있는 오버라이딩된 함수

