# kvstore/CompletionObject.java
- 7개의 생성자를 두었다. 
- `public static final String TAG  = CompletionObject.class.getName();` : getName()은 각 패키지명이 포함된 클래스명을 추출한다.


# kvstore/RemoteKVStore.java
- KVStoreAdaptor를 구현한 RemoteKVStore클래스. 


# kvstore/ReplicatedKVStore.java
- 데이터베이스에 저장하는 것과 키값 복제에 관련된 듯하다. (자세히는 모르겠다.)
- `private static final String KEY_REGEX = "^[^_][\\w-]{1,255}$"` : key의 정규식([참고 링크](https://en.wikipedia.org/wiki/Regular_expression))

- `public final boolean encrypted = true` : 암호화 되어 있는지
- `public final boolean encryptedReplication = true` : 암호화를 복제했는지?

- `private final PlatformSqliteHelper dbHelper` : 변수인 듯하다.
- `private final String[] allColumns` : 변수를 모아놓은 배열인 듯하다{version, remote_version key, value, time, deleted 포함됨(앞에는 PlatformSqliteHelper.KV_ 붙여짐)}

