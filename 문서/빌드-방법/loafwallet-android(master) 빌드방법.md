# 설명
- [loafwallet-android](https://github.com/pyeongtaekcoin-foundation/loafwallet-android) master브런치 프로젝트를 컴퓨터에 빌드하는 방법을 설명

# 빌드 방법
- [v1.19.0 브런치의 빌드방법](loafwallet-android(v.1.19.0)%20빌드방법.md)과 동일

# 오류 모음
- [v1.19.0 브런치의 오류](loafwallet-android(v.1.19.0)%20빌드방법.md) 참고

## partnerapi submodule 다운로드 오류 관련
- partnerapi 저장소위치가 아예 사라짐 -> github에 관련 작업이 안되있는것으로 추정

## partnerapi build(rebuild) 오류 관련
- `프로젝트/settings.gradle` 파일에서 `include ':partnerapi'` 주석처리
- `프로젝트/app/build.gradle` 파일에서 `api project(":partnerapi")` 주석처리
- NetworkModule관련 오류: partnerapi프로젝트 내에 존재하는 네트워크 관련 클래스인것으로 보임, 하지만 partnerapi가 저장소가 없어짐

## Dagger 관련
- `포로젝트/app/build.gradle`에 `annotationProcessor "com.google.dagger:dagger-android-processor:2.27"` 삽입










