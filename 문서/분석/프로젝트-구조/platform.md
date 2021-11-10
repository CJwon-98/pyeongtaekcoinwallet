# `platform`
- SPV노드에서의 토큰 거래에 관련된 것들(클래스, 인터페이스, wrapper 클래스) 모아놓은 패키지
## APIClient
- API와 통신할 때 사용하는 Client 클래스
## BRGeoWebSocketHandler
- GeoLocationManager관련 핸들러 
## BRHTTPHelper
- HTTP 여러 기능 도와주는 클래스
## GeoLocationManager
- 인터넷을 통해 위치 찾는 작업 관련 클래스
## HTTPServer
- HTTP로 서버 여는 클래스


# `platform.entities`
- 거래 관련 정보를 클래스로 담아놓은 것들 모음 패키지
## TxMetaData
- 트랜잭션 메타 데이터 담는 클래스
## WalletInfo
- 지갑 정보 담는 클래스


# `platform.interfaces`
- platform에서 사용되는 인터페이스 모음 패키지
## KVStoreAdaptor
- Key-Value(hashmap 과 비슷함) 데이터 베이스 API
## Middleware
- [MiddleWare](https://dbrang.tistory.com/693) 관련 API
## Plugin
- 플러그인 관련 API (자세히 모름)

# `platform.kvstore`
- 
## CompletionObject
- 완료된 객체(트랜잭션인지 다른것인지 구분 불가) 저장하는 클래스 틀
## RemoteKVStore
- KVStore 관리(삽입, 수정, 삭제 등) 클래스
## ReplicatedKVStore
- sql 데이터베이스에서 KVStore로 데이터 복제하는 기능 클래스

# `platform.middlewares`
- 
## APIProxy
- 
## HTTPFileMiddleware
- 
## HTTPIndexMiddleware
- 
## HTTPRouter
- 
# `platform.middlewares.plugins`
- 
## CameraPlugin
- 
## GeoLocationPlugin
- 
## KVStorePlugin
- 
## LinkPlugin
- 
## WalletPlugin
- 





















