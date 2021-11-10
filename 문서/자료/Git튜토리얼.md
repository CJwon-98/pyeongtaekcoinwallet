# Git
소스코드 관리 프로그램

# Github
소스코드 관리 프로그램인 Git을 사용해서 여러사람과 프로젝트를 같이 진행할 수 있게 도와주는 공유 사이트

# 기초 명령어
> `git bash` 프롬프트 사용(linux)  
> `<>`: 필수, `[]`: 선택
- `git init`: 현재 폴더에서 git을 쓰겠다 선언
- `git add .`: git프로그램에게 작업 완료했다고 관리해달라고 등록해주기
- `git commit -m "메세지"`: 작업을 완료한것에 메세지 남기기
- `git push [origin main]`: 자신 컴퓨터에 있는 프로젝트를 Github에 올리기
- `git pull [origin main]`: Github에 있는 프로젝트의 최신 파일들을 모두 가져오기
- `git clone <저장소 url>`: 저장소 url의 프로젝트를 현재 폴더에 다운로드
- `cd <경로>`: `경로`로 폴더를 이동
- `pwd`: 현재 파일 위치 출력
- `git status`: 현재 상황 정리해서 보여줌
- `Ctrl + C`: 취소(명령어 아님)


# 사용법
## Git과 Github 계정 연동
1. `git config --global user.name "Github 계정 닉네임"`: git에 이름 등록
2. `git config --global user.email "Github계정 이메일"`: git에 이메일 등록
3. `git config -list`: git에 계정 등록이 잘 됬나 확인
※ 중간에 Github사이트 계정 연동 나오면 진행하기

## 프로젝트 다운받기
1. `git init`
2. `git clone <저장소 url>`
3. `cd <프로젝트 이름>`
4. 사용

## 프로젝트 Github에 올리기(업데이트하기)
1. `git add .`
2. `git commit -m "메세지"`
3. `git pull origin main` 
> - 내가 수정하기전에 누가 먼저 Github에 수정파일을 올려놓으면 그걸 다운받아서 최신상태에서 올리겠다  
> - 충돌(conflice) 일어나면 해당 파일 수정후 다시 `add`, `commit`
4. `git push origin main`

## 새로운 프로젝트 올리기
1. Github사이트에서 프로젝트 저장소 만들기(되도록 아무런 파일 없이)
1. `git init`: git 선언
2. `git add .`: 관리 부탁
3. `git commit -m "msg"`: 메세지 작성
4. `git branch main`: 생략
5. `git checkout main`: 생략
6. `git branch -d master`: 생략
7. `git remote add origin <만든 Github저장소 url>`: 저장소 git에 등록
8. `git push origin main`: 저장소에 업로드



