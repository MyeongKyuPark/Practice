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

## 사건1 진술서
fatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream practice master

#### 사건1 진술서 해석본 (의역)
오류: 현재 브랜치 마스터가 상위(상류) 브랜치가 없다. 현재 브랜치를 푸시하고 원격 저장소를 업스트림으로 설정하기 위해서는 git push --set-upstream practice master 를 사용하라

## 내 의문(생각)
1. 알려주는건 고마운데 업스트림 브랜치 개념이 뭘까?
2. 찾다보니까 master 빼먹은걸 발견했다.
3. git remote add "site" 했는데도 불구하고 왜 업스트림이 없는건가.

#### (WIU@) 1. Git에서 업스트림이란?
업스트림은 말 그대로 물을 흘려 보내는 곳. 다운스트림은 물을 받는 곳.

ex) 내가 github에서 자료 pull 하면 github가 상류 (데이터를 흘려 보낸다). 내 컴퓨터가 하류 (데이터를 받는다)

#### 2. master 붙여봤다.
## 사건2 진술서
fatal: 'pratice' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

또 뭔가 발생했다1(ㅋㅋ;). 실질적인거 하나라도 건져가자.

#### 사건2 진술서 해석본 (의역)
오류: 'practice'가 깃 저장소에 안 보인다.
오류: 원격 저장소에서 읽을 수가 없다.

접근 권한이 있는지랑 저장소가 존재하는지 확인해봐라

=> 확인해보자.
깃허브에 pracice라는 저장소 만들었고 존재한다. 

내가 입력한 코드는 git push practice master 이었다. 

이게 의미하는 바에서 3번째 4번째 단어의 역할을 다시 찾아보자. 

git push는 원격 저장소에 코드 변경분을 업로드하기 위해 사용되는 Git 명령어다. 확인

찾아보니까 git push <저장소명> <브랜치명> 이다. 

내가 입력한 코드는 '나 코드 변경분 업로드 하기 위해 practice 라는 저장소명에 브랜치명은 master로 보낼거야'다. 

저장소는 존재하는데 권한을 다시 확인해보자.

Direct Access. 나만 기여할 수 있다고 하니까 되야하는거 아닌가?

git clone에 대해 확인해보자.

#### (WIU@) 3. git remote add "site" 했는데 왜 해당 사이트가 업스트림이 안되는 걸까?


____

github에서 하라는대로 해서 우선 해결됐다.

아직까지 배경지식이 없어서 뭘 할 때마다 사건이 터져나와서 일단락하고 원인은 유튜브나 구글링을 하면서 공부하다가 나중에 먼 훗날 되돌아보지 않을까 싶다.

우선 github에서 하라는 거는
git remote add origin "site"
git branch -M main
git push -u origin main

였고 이대로 하니까 됐다.
참고로 branch -M main 안하고 바로 3번째로 가니까 

error: src refspec main does not match any

이렇게 떴었다. 있다는 거만 알아두자.

그리고 git clone 하니까 Practice라는 repos가 복제됐다. 여기서 하지 않아서 발생한 일이지 않을까 싶지만 우선 천천히 하자. 