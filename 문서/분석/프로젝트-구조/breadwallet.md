# `breadwallet`
- breadwallet 관련 패키지

## BreadApp
- 앱 시작 클래스
***
# `breadwallet.exceptions`
- breadwallet관련 예외 패키지

## BRKeystoreErrorException
- Key 저장 에러 관련 예외 클래스

## CertificateChainNotFound
- 인증된 체인 못 찾은 예외 클래스

## PaymentRequestExpiredException.java
- 지급 요청이 만료된 예외 클래스

***
# `breadwallet.presenter`
- breadwallet 관련 사용자에게 보여주기 위한 패키지

# `breadwallet.presenter.activities`
- 액티비티 관련 클래스 모음 패키지

## BreadActivity
- 대표 activity(아래 activity들을 다 import하고 있음)
## DisabledActivity
- 문제가 있는 것과 관련 액티비티
## InputWordsActivity
- 입력어와 관련된 액티비티(여러 나라 언어 포함됨)
## LoginActivity
- 로그인 관련 액티비티
## PaperKeyActivity
- [paperkey](https://wiki.archlinux.org/title/Paperkey)와 관련된 액티비티
## PaperKeyProveActivity
- [paperkey](https://wiki.archlinux.org/title/Paperkey) 증명에 관련된 액티비티
## ReEnterPinActivity
- pin(개인식별번호) 재입력에 관련 액티비티
## SetPinActivity
- pin(개인식별번호) 설정 관련 액티비티
## UpdatePinActivity
- pin(개인식별번호) 업데이트 관련 액티비티

# `breadwallet.presenter.activities.camera`
- 액티비티에서 카메라에 관련된 패키지

## AutoFitTextureView
- 주어진 종횡비에 맞게 크기를 자동으로 조절, 카메라 미리보기를 표시 관련 클래스 ([참고 링크](https://quinnfreedman.github.io/Camera3/com/avalancheevantage/android/camera3/AutoFitTextureView.html))

## CameraActivity
- 카메라에 관한 액티비티

## ScanQRActivity
- QR코드를 스캔 관련 액티비티

# `breadwallet.presenter.activities.intro`
- 인트로(앱 실행시키면 나오는 화면)에 관련 액티비티를 모은 패키지

## IntroActivity
- 인트로(앱 실행시키면 나오는 화면)에 관련 액티비티

## RecoverActivity
- 인트로 화면 복구 관련 액티비티

## WriteDownActivity
- 기록(적는 것) 관련 액티비티

# `breadwallet.presenter.activities.settings`
- 

# `breadwallet.presenter.activities.util`
- 액티비티에서 활용(utils)에 관련 클래스를 모은 패키지

## ActivityUTILS
- 액티비티 활용에 관련 클래스(상태 바 색깔 설정 등) 

## BRActivity
- 액티비티 관련 클래스(특징: 인트로 패키지 인포트, 지갑이 잠겨있으면 잠겨있다고 표시 등)

# `breadwallet.presenter.customviews`
- 

# `breadwallet.presenter.entities`
- 
## RequestObject
- 요청 클래스(address, r, amount, label, message, req)
## TxItem
- 트랜잭션 구성 클래스 (타임스탬프, 블록넘버, 수수료, 해시크기 등)

# `breadwallet.presenter.fragments`
- 프래그먼트 관련 패키지
- 프래그먼트:  하나의 액티비티에 결합하여 창이 여러 개인 UI빌드 가능
## DynamicDonationFragment
- 
## FragmentBuy
- 구매 프래그먼트
## FragmentFingerprint
- 지문 API를 사용한 프래그먼트
## FragmentGreetings
- ok버튼 프래그먼트 (인사말? 대답 관련 프래그먼트)
## FragmentManage
- 관리 프래그먼트
## FragmentMenu
- 메뉴 프래그먼트
## FragmentPhraseWord
- 어구? 
## FragmentPin
- 핀 프래그먼트
## FragmentReceive
- 주소 받는 프래그먼트(QR이미지 관련)
## FragmentRequestAmount
-
## FragmentSend
- 송금 프래그먼트
## FragmentSignal
- 신호 관련 프래그먼트 (터치 방지)
## FragmentSupport
-
## FragmentTransactionDetails
- 트랜잭션 상세 프래그먼트(view pager 사용, TxItem포함)
## FragmentTransactionItem
- 트랜잭션 프래그먼트

# `breadwallet.presenter.interfaces`
- 

***
# `breadwallet.tools`
- breadwallet관련




***
# `breadwallet.wallet`
- breadwallet관련 
