# 설명
- [Github loafwallet-android 프로젝트(v1.19.0)](https://github.com/pyeongtaekcoin-foundation/loafwallet-android/tree/v1.19.0)의 v1.19.0 브런치 포크
- submodule 종속성 제거 후 파일들 프로젝트 내에서 그대로 사용
> `프로젝트/app/src/main/jni/loafwallet-core`  
> `프로젝트/app/src/main/jni/loafwallet-core/sec256k1`  
> `프로젝트/app/src/main/secp/sec256k1`  
- 포트번호, 코인이름, 프로토콜 설정값을 바꿔서 사용할 예정
- [문서](문서) 폴더에 모든 정보 정리
- [loafwallet-android-kiosk 프로젝트 존재](https://github.com/olivingcoin/loafwallet-android-kiosk)
---

# 주의사항
- 프로젝트를 올리기전에 꼭 패스해야 할 테스트 목록
```yml
- Rebuild
- AVD 앱 실행
```

---

# 빌드 방법
- 원본 [loafwallet-android](https://github.com/pyeongtaekcoin-foundation/loafwallet-android/)프로젝트가 아니라, 포크된 현재 프로젝트의 빌드 방법 설명

## 1. 폴더 생성
- 작업 폴더 생성


## 2. git 다운로드

- git은 소스코드 관리 프로그램, Github싸이트와 연결하기 위해서 필요함

- 명령어로 관리, 모든 명령어는 git 으로 시작함

- 다운로드 링크: https://git-scm.com/downloads



## 3. loafwallet-android 프로젝트 다운로드

- loafwallet-android 링크: https://github.com/pyeongtaekcoin-foundation/loafwallet-android

- git프로그램을 사용해서 github에 있는 loafwallet-android 프로젝트를 자신 컴퓨터에 다운로드

- 실행방법:

1. 만든 폴더로 들어가기

2. 폴더의 빈공간 우클릭 "Git Bash Here" 로 커맨드 창 실행

3. 커맨드 창에 밑의 명령어 순서대로 입력해서 프로젝트 자신 컴퓨터로 다운로드

```cmd
git clone https://github.com/olivingcoin/loafwallet-android.git
```


## 4. JDK 8 다운로드

- JDK는 자바로 개발할 때 사용할 떄 필요한 필수 라이브러리,  모음

- 다운로드 링크: https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html

- oracle 사이트 회원가입 필요

- 파일 실행 후 환경변수 설정 (이미 존재하는 자바 환경변수 확인)

- cmd에서 `java -version`으로 환경변수 확인


## 5. Android Studio 다운로드

- Android Studio는 안드로이드 어플을 개발하기 위한 프로그램

- 링크: https://developer.android.com/studio

- SDK란 안드로이드 어플 만들 떄 사용하는 도구 모음

- Android Studio에서 `Setting > Appearance & Behavior > System Settings > Android SDK` 에서 SDK 설치된 위치 확인, 11버전 설치

- SDK 환경변수 등록: https://heavenlake.tistory.com/37 (ANDROID_HOME 변수 사용해서 등록)

- SDK version들은 app/build.gradle에 자동으로 맞춰져 있음( `Compile Sdk 30`, `Target Sdk 30`, `Min Sdk 23`)


## 6. NDK, SDK 다운로드
### NDK
- NDK는 안드로이드 앱 개발할 때 Java언어 외의 언어가 필요할 때 필요한 라이브러리 (예. C언어)

- NDK r15c 버전 다운로드 링크: https://developer.android.com/ndk/downloads/older_releases.html

- `프로젝트 > local.properties`에서 밑의 ndk.dir 경로 직접 추가 (NDK는 SDK폴더 안의 ndk 폴더에 놓기, 없으면 SDK 폴더 안에 그냥 넣기)
> SDK주소 확인하는법: `File > Setting > Appearance & Behavior > System Settings > Android SDK` 에 Android SDK Location에 나와있음
```
// 생략
ndk.dir={ndk 폴더 경로}
```
- Gradle Build sync 맞추기 (`Try Again` 클릭)
### SDK
- sdk 버전 30으로 맞추기
- `File > Setting > Appearance & Behavior > System Settings > Android SDK` 들어가서 `Android 11.0 (R)` 체크하고 다운로드 받기

## 7. google-services.json 
- firebase 관련 파일
- 실제 프로젝트 앱의 `google-services.json` 파일을 firebase에서 다운받아서 사용해야 함
- [파일 다운로드](https://github.com/olivingcoin/OlivingCoin-android-wallet/blob/main/%EB%AC%B8%EC%84%9C/%EB%B9%8C%EB%93%9C-%EB%B0%A9%EB%B2%95/google-services.json) (우클릭후 다른이름으로 저장)
- google-services.json만드는 법: https://lakue.tistory.com/37
- `프로젝트 > app` 폴더에 `google-services.json`의 파일이름으로 넣어야 함


## 8. 최종 다시 빌드
- `Build > Rebuild Project` 실행
- BUILD SUCCESS 뜨면 성공


## 9. 에뮬레이터 실행
- `Tools > AVD Manager`에서 기본으로 설정된 새로운 AVD(Pixel 2) 생성 (API 30 다운로드)
- 암호화폐 지갑 보안문제로 기본적인 휴대폰 잠금을 설정해야 함: 앱 실행 전 `Tools > AVD Manager`에서 AVD 실행후에 (화면에서 `Settings > Security > Screen lock > Pattern`에서 패턴 `ㄱ`모양(순서:`1 > 2 > 3 > 6 > 9`) 로 설정하기)
- 앱 실행
<img src="AVD_work_screen.PNG" width="150" height="250">





# 오류 모음
## loafwallet/app/build.gradle 파일이 오류가 날 떄 + 대부분 상황에서 
- `File -> Invalidate Chache / Restart` 해보기


## 블루스크린 뜰 때 (에러코드: IRQL_NOT_LESS_OR_EQUAL)
- 가상화 세팅이 안되서 생긴 오류: `SDK Manager > SDK Tools`의 목록에서 `Intel x86 Emulator Accelator (HAXM installer))` 다운로드 받기
- 참고: https://stackoverflow.com/questions/60732992/android-studio-bsod-when-running-virtual-device


## AVD 먹통(까만 화면 지속)
- `Tools > AVD Manager` 에서 오른쪽 화살표에서 `Cold Boot Now` 클릭
![cold_boot](AVD_cold_boot.PNG)


## 에러 메세지
```cmd
Execution failed for task ':app:clean'.
> Unable to delete file 'C:\Users\ljh99\Desktop\CryptoCurrency\OlivingCoin-android-wallet\app\build'

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output. Run with --scan to get full insights.
```
- `File > Invalidate Caches / Restart...` 하고 다시 Rebuild 하기(Rebuild 여러면 해봐야 함)












