# 설명
프로토콜 변수 분석


# 분석 방법
- ❗**블럭체인 개념과 관련있는 설정값만 주로 정리하기** (관련없는 설정값은 매우 간단히 설명 or 모르면 건너뛰기)
- 파일 간단 설명 적기
- 설정값 관련 개념도 간단히 정리
- define으로 선언된 설정값(상수)만 분석 (하지만, define으로 선언된 매크로는 분석하지 말기), (`Ctrl + F` 눌러서 `define` 단어 찾으면 됨)
- 파일에 써있는 주석 참고하기
- 소스내에서 쓰이는 부분 근처가봐서 추측
- 설정값 이름으로 간단히 추측


# 참고 링크
- loafwallet 프로토콜 코어: https://github.com/pyeongtaekcoin-foundation/loafwallet-core/tree/2ea83a2abb82c208900cd098dcb4239cd5a90d7d

- Bitcoin 프로토콜 설명 링크: https://developer.bitcoin.org/devguide/

- 암호화폐 프로토콜 변수 위키(bitcoin기준): https://en.bitcoin.it/wiki/Protocol_documentation#Message_types

- BIP 관련 저장소 링크: https://github.com/bitcoin/bips (사이트 자체는 설명이 별로 없음, 하지만 관련 블럭체인 관련 개념 있으면 정리)



# 분석 담당
## 최지원
- BRAddress.c
- BRAddress.h
- BRArray.h
- BRBIP32Sequence.c
- BRBIP32Sequence.h
- BRBIP38Key.c
- BRBIP38Key.h

## 이정한
- BRBIP39Mnemonic.c
- BRBIP39Mnemonic.h
- BRBIP39WordsEn.h
- BRBase58.c
- BRBase58.h
- BRBloomFilter.c
- BRBloomFilter.h
- BRCrypto.c
- BRCrypto.h
- BRInt.h
- BRKey.c
- BRKey.h
- BRMerkleBlock.c
- BRMerkleBlock.h
- BRPaymentProtocol.c
- BRPaymentProtocol.h
- BRPeer.c
- BRPeer.h

## 김윤영
- BRPeerManager.c
- BRPeerManager.h
- BRSet.c
- BRSet.h
- BRTransaction.c
- BRTransaction.h
- BRWallet.c
- BRWallet.h

# 정리 형식
```
# 파일 이름
- 파일 간단한 설명
- `상수명1`: 역할
- `상수명2`: 역할
- `상수명3`: 역할

# 파일 이름2
- 파일 간단한 설명
- `상수명1`: 역할
- `상수명2`: 역할
- `상수명3`: 역할

# 파일 이름3
- 파일 간단한 설명
- `상수명1`: 역할
- `상수명2`: 역할
- `상수명3`: 역할
```


# PC 프로토콜 설정값과 동기화 방법 문서
- [링크](https://github.com/QvingCoin/QVingCoin-android-wallet/blob/main/%EB%AC%B8%EC%84%9C/%EB%B6%84%EC%84%9D/%ED%94%84%EB%A1%9C%ED%86%A0%EC%BD%9C-%EC%84%A4%EC%A0%95%EA%B0%92/PC%ED%94%84%EB%A1%9C%ED%86%A0%EC%BD%9C%EA%B3%BC%20%EC%84%A4%EC%A0%95%EA%B0%92%20%EB%8F%99%EA%B8%B0%ED%99%94.md)
