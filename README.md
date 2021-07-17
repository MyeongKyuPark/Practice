# 입맛대로 고르는 Git 코드

## 위치

pwd: 현재 위치

ls: 폴더 내용보여줘. 리스트

ls -a: 숨긴파일까지 보여줘

cd 폴더: 폴더로 이동해줘. change directory.

~: 홈 디렉토리

.: 전체 선택

..:상위폴더 (나갈래)


## 생성/삭제

mkdir 폴더이름: make directory 폴더

rm -r 폴더이름: remove 폴더

touch 파일: 파일 생성

rm 파일: 파일 삭제

mv 파일 파일: `여기`

cp 파일 ./파일: `여기`

clear: 화면 정리


## git 환경만들기

git --version: git version 확인

git init: git 폴더로 권한부여 (.git 파일 생성)

git status: 상태확인 (변화여부)

git add 파일: 사진찍기 (staging area)

git commit -m "이름": 복구파일버전 생성

git config --global user.name '이름': 처음 git 생성할때 이름

git config --global user.email '이메일': 처음 git 생성할때 이메일

git log: 업데이트 내용에 대한 로그

git checkout 코드 : `여기` (master) 에서 코드로 변환됨.

git checkout master : `여기` 마스터로 전환

cat: `여기` 해보니까 빠져나와지지 않음. 메아리침.

cat config: `여기`

cat description: `여기`

code : Visual Studio Code 실행

git diff 파일 : 안에 입력된 내용 보여줘. 나갈땐 esc 연타후 q

git remote: 버전출력

git remote 저장소별명 저장소주소

git remote add origin 사이트 : 분산 사이트에 저장 (e.g. github)

git remote -v : 연결되있는 모든 분산 데이터 repos. verbose (말이많은). 상세하게 출력

git push: 원격저장소에 코드 백업

git push [저장소별명] [브랜치이름]:

git remote remove origin: 기존의 저장소와의 연결 끊기 

## 찾아볼 거!

nano 파일 : `여기` 만들고 수정까지. 실습요함. 

> cf) 특이사항 발생시 
> :!q : 이상한 곳 탈출
> q: 탈출

ctrl c/ ctrl v: `여기`
ctrl ins/shift ins : 복사 붙여넣기

## 순서

mkdir recap(폴더 만들기)

git init (git 권한 주기)
touch hello.md
code. (코드작성)
git add hello.md (사진)
git commit -m 'hello.md' (버전)
github 가서 repos 만들기
git remote add 별명 주소
git remote -v 확인
git push origin 별명

## 궁금한 코드

1. 실행한 코드 취소




## 참조사항

1. `여기` 는 작성자가 공부하려고 체크한 부분
2. `여기1` 는 실습이 필요함
3. 사용자가 경험한 것을 기초로 작성