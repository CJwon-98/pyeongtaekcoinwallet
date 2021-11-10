# 설명
- 키오스크에서 Order안에 있는 금액으로 QR코드를 업데이트 해서 사용자에게 보여줘야 함



# QR 코드 화면
- `receive`, `reqeust` 로 2개의 화면을 가짐
- `receive`, `reqeust` 둘 다 같은 xml 파일(`fragment_receive.xml`)을 사용
## receive 화면
<img src="../이미지/QR_receive_fragment.jpg" width=30%><>
- QR 코드를 띄우고 상대방이 캡쳐해서 금액을 정해서 보내는 방법
- `BreadActivity`에서 `FragmentReceive` fragment 열음
```java
BRAnimator.showReceiveFragment(BreadActivity.this, true);
```
- 금액 입력에 QR코드 재생성 코드를 여기서 등록해 놓음
```java
BRWalletManager.getInstance().addBalanceChangedListener(new BRWalletManager.OnBalanceChanged() {
    @Override
    public void onBalanceChanged(long balance) {
        updateQr();
    }
});
```

## request 화면
<img src="../이미지/QR_request_fragment2.jpg" width=30%></img>
<img src="../이미지/QR_request_fragment1.jpg" width=30%></img>
- 요구할 가격을 정해놓고, 상대방이 캡쳐해서 정해진 금액을 보내는 방법
- 금액을 설정할 때마다 QR코드가 변경됨
- `FragmentReceive`에서 `FragmentRequestAmount` fragment 열음
```java
BRAnimator.showRequestFragment(app, receiveAddress);
```

# 순서
1. RequestFragment 띄우기
2. BRWalletManager.getInstace().onBalanceChanged(balance) 호출해서 가격 설
3. 자동으로 QR업데이트 됨
