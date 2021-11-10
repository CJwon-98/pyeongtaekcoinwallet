 

# BRPeerManager.java 클래스 역할 및 특징

### 참고
`함수의 역할이 정확한지는 잘 모르겠음.`

## 역할: 
- 피어를 관리하는 클래스


## 특징
- 


* * *

# 변수 역할

* * *
# 메소드 역할

## getInstance()
- 싱글톤 패턴을 사용하는 함수
- 싱글톤이란 고정된 메모리 영역을 사용하여 메모리 낭비를 줄이고 공통된 객체를 사용할 때 매번 객체를 새로 생성하지 않는 방식
- [참고 링크1](https://myhappyman.tistory.com/35)
- [참고 링크2](https://elfinlas.github.io/2019/09/23/java-singleton/#:~:text=%EA%B7%B8%EB%A0%87%EB%8B%A4%EB%A9%B4%20%EC%8B%B1%EA%B8%80%ED%86%A4%20%ED%8C%A8%ED%84%B4%EC%9D%84,%EC%99%80%20%EA%B3%B5%EC%9C%A0%EA%B0%80%20%EC%9A%A9%EC%9D%B4%ED%95%98%EB%8B%A4.)




## syncStarted
- 동기화 시작하는 함수


## syncSucceeded()
- 동기화 성공할 때 사용하는 함수
- if문으로 app == null 실행되기 전 getBreadContext()에서 currentActivity가 null이면 SyncReceiver.app를 반환하고 null이 아니면 currentActivity를 반환한 값이 if문에서 app값이 됨.


## synFailed()
- 동기화 실패할 때 사용하는 함수
-



## txStatusUpate()
- 트랜잭션 상태를 업데이트하는 것과 관련된 함수
-




## saveBlocks(final BlockEntity[] blockEntities, final boolean replace)
- 블록을 저장하는 함수?(블록의 길이를 저장하는 듯함)
- getBreadContext()에서 currentActivity가 null이면 SyncReceiver.app를 반환하고 null이 아니면 currentActivity를 반환한 값이 if문에서 ctx값이 됨.





## savePeers(final PeerEntity[] peerEntities, final boolean replace)
- 피어를 저장하는 함수
-



## networkIsReachable()
- 네트워크가 연결 가능하기 위한 함수
-


## deleteBlocks()
- 블록을 삭제하기 위한 함수
-



## deletePeers()
- 피어를 삭제하기 위한 함수

## updateFixedPeer(Context ctx)
- 고정된 피어를 업데이트하기 위한 함수
- if문으로 실패하면 updateFixedPeer: Failed to updateFixedPeer with input: %s
- 성공하면 updateFixedPeer: succeeded


## networkChanged(boolean isOnline)
- 네트워크를 교환하기 위한 함수
- if문에서 isOnline값이 참이면 실행




## addStatusUpdateListener(OnTxStatusUpdate listener)
- 업데이트 상태 수신기를 더하기 위한 함수
- [참조 링크](https://developer.android.com/reference/com/google/android/things/update/StatusListener)


## removeListener(OnTxStatusUpdate listener)
- 업데이트 상태 수신기를 제거하기 위한 함수
- 




## setOnSyncFinished(OnSyncSucceeded listener)
- 동기화 설정이 끝났을 때 사용하는 함수
- 





## updateLastBlockHeight(int blockHeight)
- 마지막 블록 높이를 업데이트를 하기 위한 함수
- 
