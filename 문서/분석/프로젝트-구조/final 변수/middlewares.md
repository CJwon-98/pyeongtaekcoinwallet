# middlewares/APIProxy.java
- final 변수와 문자열 배열
- `MOUNT_POINT` : 포인트 양?("/_api")
- `SHOULD_VERIFY_HEADER` : 검증한 헤더? ("x-should-verify")
- `SHOULD_AUTHENTICATE` : 인증하는 것?("x-should-authenticate")
- `String[] bannedSendHeaders` : 보내는 것이 금지된 헤더(문자열 배열)
- `String[] bannedReceiveHeaders` : 받는 것이 금지된 헤더 (문자열 배열)


# middlewares/HTTPFileMiddleware.java
- 
- `DEBUG_URL` : 테스트를 위해 수정(NULL)



# middlewares/HTTPIndexMiddleware.java
- final이 없음


# middlewares/HTTPRouter.java
- final이 없음

----

# middlewares.plugins/CameraPlugin.java
- Plugin를 구현함.
- `Request baseRequest` : handle의 매개변수
- `HttpServletRequest request` : handle의 매개변수
- `HttpServletResponse response` : handle의 매개변수
- `final Context app` : getBreadContext 함수의 결과값을 저장



# middlewares.plugins/GeoLocationPlugin.java
- Plugin를 구현함
- `final boolean granted` : handleGeoPermission의 매개변수



# middlewares.plugins/KVStorePlugin.java
- final이 없음, Plugin를 구현함
- `` :
- `` :


# middlewares.plugins/LinkPlugin.java
- final이 없음, Plugin를 구현함
- `` :
- `` :

# middlewares.plugins/WalletPlugin.java
- Plugin를 구현함
- `final JSONObject restJson` : sendBitIdResponse의 매개변수
- `final boolean authenticated` : sendBitIdResponse의 매개변수
