# 설명
- Git에서 다른 프로젝트의 Github을 참조해서 사용하는 기능이 `submodule`이다

# submodule 제거 순서
- 종속성 제거할 서브모듈 2개 
> `프로젝트/app/src/main/jni/loafwallet-core`
> `프로젝트/app/src/main/secp/sec256k1`

1. 프로젝트 폴더로 들어간다
2. `.gitmodules` 파일에서 삭제할 서브모듈 부분을 제거한다
3. `git add .gitmodules`로 .gitmodules가 바뀐것을 stage시킨다
4. `.git/config`에서 삭제할 서브모듈 부분을 제거한다
5. `git rm --cached <제거할 서브모듈 경로>`입력
6. `.git/modules`에 들어가서 삭제할 서브모듈 폴더를 제거한다
※ `프로젝트/app/src/main/jni/loafwallet-core` 폴더 안에 `sec256k1`폴더가 또 있는데 이것도 `프로젝트/app/src/main/secp/sec256k1` 폴더 복사해서 넣어줌







# 참고
- https://stackoverflow.com/a/1260982/14850276
