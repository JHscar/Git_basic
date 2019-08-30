# Git이란?
### 깃(Git/git)은 프로그램 등의 소스 코드 관리를 위한 분산 버전 관리 시스템 이다.

## 기본 용어
* **커맨트 라인(Command Line) : 깃 명령어를 입력할 때 사용하는 컴퓨터 프로그램, 맥에선 터미널이라고 한다.**

* **저장소(Repository) : 프로젝트가 거주(live)할 수 있는 디렉토리나 저장 공간, 깃허브 사용사는 종종 “repo”로 줄여서 사용한다. 자신의 컴퓨터 안의 로컬 폴더가 될 수도 있고, 깃허브나 다른 온라인 호스트의 저장 공간이 될 수도 있다.**

* **커밋(Commit) : 커밋을 하게 되면 이전의 어떠한 상태로 재평가,복원할 수 있는 체크포인트를 가질 수 있다.**

* **브랜치(Branch) : 가지 또는 분기점을 의미하며, 작업을 할때에 현재 상태를 복사하여 Branch에서 작업을 한 후에 완전하다 싶을때 Merge를 하여 작업을 한다.**


## Git 사용하기 기초 용어
### git init
버전관리 하고싶은 폴더에서 초기화를 하는 준비

### git branch
> * 독립적인 공간을 만든다.  
> * 새로 만든 branch lab1은 master와 완전히 동일한 상태를 가진 공간.  
> * 브랜치에서 수정을 한 후 커밋하면 lab1에만 기록되며 master 브랜치에는 어떤 영향도 주지 않는다.  
> * 원하는 만큼 빠르게 branch를 만들 수 있다.  
> * 실험 중 다른 브랜치로 돌아가야 할 떄 : checkout master 로 head를 옮겨야 한다.(cf > 작업 중인 위치를 가르키는 가상의 커서가 존재하는데 이를 git에서는 HEAD라 한다.)  
> * 실험 성공 : lab1 브랜치의 내용을 마스터 브랜치와 병합(Merge)한다.  
> * 실험 실패 : lab1 브랜치를 삭체한다.  

### checkout
독립된 작업 공간인 브랜치를 자유롭게 이동할 수 있다.

### git commit
의미있는 수정 작업이 끝났을 때 마침을 알리는 작업

### pull
리모트 저장소의 변경된 내용을 로컬(내 컴퓨터) 저장소에 적용하는 작업을 pull이라 한다.

### master
git init을 했을 때, default로 만들어지는 가지가 ‘master’이다.
 

# Github에 소스코드 올리기
### 1) 레포지토리 생성
Github 홈페이지([링크](https://github.com))에서 가입을 한 후 repository를 생성합니다.
(repository를 생성한 후 READ.me를 읽어보시면 앞으로 소개할 내용이 나온다)

### 2) 업로드할 폴더로 이동
커맨더 창을 통해, 깃헙에 업로드할 파일이 있는 폴더로 이동합니다.
**==> cd 폴더경로**

### 3) init
커맨더 창에서 아래의 명령어를 통해, 위의 폴더로 git이 추적할 수 있도록 .git폴더를 생성합니다.
즉, local repository를 생성하는 것입니다.
**==> git init**

### 4) 상태 확인
git이 버전관리 대상 파일들의 상태를 파악합니다.
**==> git status**
* 명령어가 동작하지 않을 때 에러 확인
* 내가 작업한 파일 외에 다른 파일이 수정되진 않았는지 확인

### 5) add
버전 관리할 파일들을 추가합니다.
git add 파일 명령어는 특정 파일을 추가하는 명령어이며, 아래의 명령어는 변경 모든 파일을 local repository에 추가하는 명령어 입니다.
**==> git add (관리할 파일명)**

### 6) commit
commit 메시지를 작성합니다.
**==> git commit -m “메시지내용**
-m 옵션은 간단하게 한줄로 메시지를 작성하기 위함이며, 긴 메시지 작성이 필요하다면 git commit 명령어만 실행하면 됩니다.

### 7) remote 등록
Remote repository를 등록합니다.
**==> git remote add origin {remote repository 주소}**
origin은 remote repository의 별칭을 의미하며, 매 번 remote repository의 주소를 입력하는 것이 귀찮으므로 별칭을 사용합니다.
일반적으로 origin을 사용한다.

### 8) push
commit 한 내용을 remote repository에 push(업로드) 합니다.
**==> git push origin master**
master는 브랜치(branch)의 이름이고, remote repository를 생성하면 기본적으로 master 브랜치가 생성됩니다.
(참고로 브랜치는 독립적인 작업 공간을 의미하며, 브랜치 덕분에 협업이 수월해지기 때문에 꼭 알아둬야 하는 개념)

master가 아닌 다른 branch로 push 하고 싶으면, 아래와 같이 master를 특정 브랜치명으로 바꿔서 명령어를 실행하면 됩니다.
**==> git push origin {브랜치명}**

### 9) config 설정
git을 설치한 후 특별한 설정을 하지 않았다면, Github 이메일 주소 및 비밀번호를 입력하라고 합니다.
이메일 주소와 비밀번호를 입력하면 소스 코드가 Github로 푸시가 잘 된다.









