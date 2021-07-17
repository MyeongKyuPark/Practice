# 오늘의 오류
## 오늘 하려고 했던 거
어제 배웠던 push pull을 활용해보자.

## 사건 경위 (시간순)
0. cd ~
1. mkdir practice
2. git init
3. code
4. git add [file]
5. git commit -m "practice"
6. git remote add "site"
`7.` git push practice

## 사건 진술서
fatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream practice master

## 사건 진술서 해석본 (의역)
오류: 현재 브랜치 마스터가 상위(상류) 브랜치가 없다. 현재 브랜치를 푸시하고 원격 저장소를 업스트림으로 설정하기 위해서는 git push --set-upstream practice master 를 사용하라

## 내 생각
1. 알려주는건 고마운데 업스트림 브랜치 개념이 뭘까?
2. 우선은 원격 저장소가 업스트림이 되어야 하나보다.
3. git remote add "site" 했는데도 불구하고 왜 업스트림이 없는건가.

## (WIU@) Git에서 업스트림이란?
업스트림은 말 그대로 물을 흘려 보내는 곳. 다운스트림은 물을 받는 곳.

ex) 내가 github에서 자료 pull 하면 github가 상류 (데이터를 흘려 보낸다). 내 컴퓨터가 하류 (데이터를 받는다)

