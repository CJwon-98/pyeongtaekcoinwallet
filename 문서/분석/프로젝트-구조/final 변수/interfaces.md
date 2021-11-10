# interfaces/KVStoreAdaptor.java
- 인터페이스 선언 
- `CompletionObject ver(String key)` :
- `CompletionObject put(String key, byte[] value, long version)` : 놓다?
- `CompletionObject del(String key, long version)` : 삭제?
- `CompletionObject get(String key, long version)` : 얻는 것?
- `CompletionObject keys()` : 키?

# interfaces/middleware.java
- 인터페이스 선언 
- `boolean handle(String target, org.eclipse.jetty.server.Request baseRequest, HttpServletRequest request, HttpServletResponse response)` : handle이란 
응용프로그램이 운영체제내에 있는 자원을 사용하려고 하는 경우 운영체제는 자신이 관리하는 자원이나 정보를 보호하기 위해 직접적인 주소 대신 필요한 자원을 구성하고 그 주소를 특정 숫자값과 연결하여 응용프로그램에게 숫자값을 알려준다. 이 때 이 숫자값이 핸들값이다. ([참고 링크](http://www.tipssoft.com/bulletin/board.php?bo_table=FAQ&wr_id=414))


# interfaces/Plugin.java
- 인터페이스 선언 
- `boolean handle(String target, org.eclipse.jetty.server.Request baseRequest, HttpServletRequest request, HttpServletResponse response)` : 이하동문
