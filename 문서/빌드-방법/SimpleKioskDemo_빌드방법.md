# 설명
- [프로젝트 저장소]
- 참고 블로그: [1], [2], [3]
- 블로그에 나온 소스코드들은 이미 [프로젝트 저장소]에 모두 작성되어 있음
- 안드로이드 앱을 키오스크에서 사용할 수 있게 해주는 기반 앱
- 기본 안드로이드에서 많은 기능을 제한해서 단순히 1가지 앱 안에서만 활동하게 제어하는 방식
- 여러 기능들을 커스텀해서 제한 가능
- 안드로이드 9이하 버전에서 동작 (정확히는 몇 기능이 10이상부터 지원 x)
- 안드로이드 기능 제한: DevicePolicyManager클래스 확인 가능
- 앱을 소유자(Owner) 권한을 부여해야 함

# 목적
- 전원이 켜지면 자동으로 loafwallet-android 앱이 실행이 되고, 키오스크 모드로 잠기는 것

## 1. 프로젝트 다운로드
- [프로젝트 저장소]
- git clone 또는 zip으로 다운로드

## 2. 안드로이드 스튜디오 준비
- AVD: API 28 준비
- 위의 다운로드한 프로젝트 불러오기

## 3. 소스코드 수정
- `app/src/main/java/net/sjava/examples/kiosk/MainActicity.java`파일의 `onCreate()` 에서 첫번째 예제 코드를 활성화 시키고,
두번째 예제코드를 비활성화 시키기 (단순히 앱을 잠그기만 하는것이 목적이기 때문에)
```java
mStartLockButton.setOnClickListener(new View.OnClickListener() {
  @Override
  public void onClick(View v) {
    // 첫번째 예제 코드
    LockUtil.lock(MainActivity.this);
    startLockTask();

    // 두번째 예제 코드
//        disableCamera(true);
//        setUserRestrictions(true);
//        setPackagesSuspended(mSuspendedPackageNames, true);
  }
});

mEndLockButton.setOnClickListener(new View.OnClickListener() {
  @Override
  public void onClick(View v) {
    // 두번째 예제 코드
//        disableCamera(false);
//        setUserRestrictions(false);
//        setPackagesSuspended(mSuspendedPackageNames, false);

    // 첫 번째 예제 코드
    LockUtil.unLock(MainActivity.this);
    stopLockTask();
  }
});
```

## 4. 실행
- AVD API 28버전 실행
- 앱 내의 `START LOCK` 클릭해서 잠그기










[프로젝트 저장소]: https://github.com/mcsong/SimpleKioskDemo
[1]: http://sjava.net/2020/05/%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-%ED%82%A4%EC%98%A4%EC%8A%A4%ED%81%ACkiosk-%EC%95%B1-%EA%B0%9C%EB%B0%9C-1-3/
[2]: http://sjava.net/2020/05/%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-%ED%82%A4%EC%98%A4%EC%8A%A4%ED%81%ACkiosk-%EC%95%B1-%EA%B0%9C%EB%B0%9C-2-3/
[3]: http://sjava.net/2020/05/%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C-%ED%82%A4%EC%98%A4%EC%8A%A4%ED%81%ACkiosk-%EC%95%B1-%EA%B0%9C%EB%B0%9C-3-3/
