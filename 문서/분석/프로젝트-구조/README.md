# 설명
프로젝트 구조 분석한 파일들 올리는 폴더

# 프로젝트 구조 분석
- `app/src/main/java/com`폴더부터 분석
- 총 185개 파일
- 클래스 역할 간단 설명
- 패키지 역할 간단 설명
- 파일 3개(`breadwallet.md`, `jniwrappers.md`, `platform.md`) 내에 자신이 맡은 것 정리 (git 충돌 나면 자신이 수정한 부분 복사해두고 수정 취소한 다음에 다시 눌러서 복사한 부분 붙여넣기)

## 정리 형식
```markdown
# `패키지 이름`
- 패키지 역할
## 클래스1 이름
- 클래스1 역할
## 클래스2 이름
- 클래스2 역할
```

## 정리 예시
```markdown
# `breadwallet`
- breadwallet 관련 패키지
## BreadApp
- 앱 시작 클래스
# `breadwallet.exceptions`
- breadwallet관련 예외 패키지
## BRKeyStoreErrorException
- Key 저장 에러 관련 예외
## CertificateChainNotFound
- 인증된 체인 못 찾은 예외
```

# `breadwallet`
- breadwallet 관련 패키지
## BreadApp
- 앱 시작 클래스
# `breadwallet.exceptions`
- breadwallet관련 예외 패키지
## BRKeyStoreErrorException
- Key 저장 에러 관련 예외
## CertificateChainNotFound
- 인증된 체인 못 찾은 예외



## 담당 파일
### 김윤영
- `breadwallet.exceptions.BRKeystoreErrorException`(처음) ~ `breadwallet.presenter.entities.PeerEntity`

### 최지원
- `breadwallet.presenter.entities.RequestObject` ~ `breadwallet.tools.security.PostAuth`

### 이정한
- `breadwallet.tools.security.RootHelper` ~ `platform.HTTPServer`(끝)




















