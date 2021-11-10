# platform/APIClient.java
- 요청을 만들고, 서명하고, 보낸다.  번들을 업데이트, 번들을 파일에 작성
- `PROTO` : proto는 API와 통신하는 데 사용할 전송 프로토콜 (http 또는 https)입니다
- `FEE_PER_KB_URL` : (" / v1 / fee-per-kb ")
- `TOKEN` : ("/token")
- `ME` : ("/me")
- `BUNDLES` : ("bundles")
- `BUNDLES_FOLDER` : (String.format("/%s", BUNDLES))
- `PRINT_FILES` : (false)
- (private타입) `text` : 
- (final MediaType) `JSON` : 
- (final InputStream) `is` : 생성자인지 객체선언인지 모르겠음(new FileInputStream(bundleFile))
- `outPutFileName` : replace의 함수 결과값을 저장?
- `outputFile` : 객체선언?
- `startTime` : currentTimeMillis 함수 결과값을 저장
- (final APIClient) `client` : (this)

# platform/BRGeoWWebSocketHandler.java
- final로 선언된 변수는 없음


# platform/BRHTTPHelpler.java
- 
- `TAG` : getName() 으로 클래스 정보를 가져오는 듯하다.



# platform/GeoLocationManager.java
- 
- (Context) `app` : getBreadContext() 함수 결과값을 저장
- `locationManager` : getSystemService 함수 결과값을 저장
- `jsonLocation` : execute 함수 결과값을 저장
- `` :


# platform/HTTPServer.java
- 
- `PORE` : 포트번호(31120)
- `URL_EA` :      (http://localhost:" + PORT + "/ea)
- `URL_BUY` :     (http://localhost:" + PORT + "/buy)
- `URL_SUPPORT` : (http://localhost:" + PORT + "/support)
- `app` : getBreadContext() 함수 결과값을 저장
