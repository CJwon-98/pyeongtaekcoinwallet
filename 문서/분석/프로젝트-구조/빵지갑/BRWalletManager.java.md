# BRWalletManager.java 클래스 역할

### 참고
`함수의 역할이 정확한지는 잘 모르겠음.`

## 역할
- 


## 특징
- private boolean으로 itInitiatingWallet(초기화된 지갑) 변수가 선언



***

# 메소드 역할

## setBalance(final Context context, long balance)
- 금액을 설정

## refreshBalance(Activity app)
- 금액을 새로 고쳐서 잔액을 확인할 경우


## getBalance(Context context)
- 금액을 얻는 함수


## BRWalletManager()
- 지갑을 관리하는 함수
- 배열 리스트 선언




## BRWalletManager getInstance()
- 싱글톤 패턴을 사용하는 함수


## generateRandomSeed(final Context ctx) [다시 한번 확인 필요]
- 




## wipeKeyStore(Context context)
- timber를 사용해서 log를 남김
- 저장한 키를 지우다


## noWallet(Context ctx)
- 지갑이 없는 경우

- 키 저장소를 사용할 수 있고 지갑에 지갑이 없다는 것을 알고 있는 경우 true
- 인증되지 않은 경우 오류가 발생하고 false가 반환되므로 실수로 지갑을 제거할 염려가 없습니다.



## noWalletForPlatform(Context ctx)
- 플랫폼용 지갑 없을 때


## isPasscodeEnabled(Context ctx)
- 암호가 가능한 경우
- 장치 암호가 활성화된 경우 true



## isNetworkAvailable(Context ctx)
- 네트워크 사용 가능 한 경우



## refreshAddress(Context ctx)
- 주소를 새로 고칠 때



## wipeWalletButKeystore(final Context ctx)
- 저장한 키를 지갑에서 지우다



## wipeAll(Context app)
- 모든 것을 지우다




## confirmSweep(final Context ctx, final String privKey) [다시 한번 확인 필요]
- 스윕이 발생하는 데 걸리는 시간은 지정된 전송 시간의 네트워크 속도에 따라 다르며 네트워크에서 스윕이 확인될 때까지 사용자 잔고에 크레딧을 적용할 수 없습니다. 이때 말하는 확인을 스윕 확인

- sweep이란 사용자 예금 주소에서 지갑으로 이체하는 것 ([참조 링크](https://github.com/iotaledger/wiki/wiki/User-deposit-address-sweeping-to-internal-exchange-addresses))
- sweep 확인에 대한 [참조 링크](https://support.coinfalcon.com/en-us/article/what-is-a-sweep-confirmation-1pdpijb/)



## publishCallback(final String message, final int error, byte[] txHash)
- 게시된 메시지에 영향을 주는 이벤트에 대한 콜백 ([참고 링크](https://developers.google.com/android/reference/com/google/android/gms/nearby/messages/PublishCallback#public-constructor-summary))

- callback: 사용자가 시스템에서 요청하는 일반적인 과정과 다르게 시스템 측에서 이벤트를 발생시켜 이를 처리해달라고 하는 것     ([참고 링크](https://jinsangjin.tistory.com/10))



## onBalanceChanged(final long balance)
- 금액을 교환




## onTxAdded(byte[] tx, int blockHeight, long timestamp, final long amount, String hash)
- 트랜잭션을 추가



## showToastWithMessage(Context ctx, final String message)
- 토스트 메시지를 보여주는 함수
- 토스트: 사용자에게 메시지를 알려 주기 위한 박스 ([참고 링크](https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=netrance&logNo=110124168554))


## onTxUpdated(String hash, int blockHeight, int timeStamp)
- 트랜잭션을 업데이트



## onTxDeleted(String hash, int notifyUser, final int recommendRescan)
- 트랜잭션을 삭제



## startTheWalletIfExists(final Activity app)
- 지갑(있는 경우) 시작



## initWallet(final Context ctx)  [다시 한번 확인 필요]
- 지갑 초기화



## addBalanceChangedListener(OnBalanceChanged listener)
- 금액을 추가, 리스너를 변경
- 리스너(listener)는 특정 이벤트를 처리하는 interface. 이벤트 발생 여부를 기다리다가, 발생시 특정 이벤트에 맞는 처리를 하는 객체. ([참고 링크](https://okky.kr/article/369831))



## removeListener(OnBalanceChanged listener)
- 리스너를 제거



## OnBalanceChanged
- 금액을 변경




## setFeePerKb(long fee)
- kb당 수수료를 설정



