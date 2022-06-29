# <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=Git&logoColor=white"/></a> git-study
>**git**을 공부하는 레포지터리입니다.

#### 📎도움 받은 강의
- [호눅스, Git과 Github 시작하기](https://www.inflearn.com/course/git-and-github/dashboard)
- [얄코, 제대로 파는 git-github](https://www.inflearn.com/course/%EC%A0%9C%EB%8C%80%EB%A1%9C-%ED%8C%8C%EB%8A%94-%EA%B9%83)
    - [강의 자료](https://www.yalco.kr/lectures/git-github/)

<img src="https://github.com/hy0417sage/study-git/blob/main/git-ylco.png" height="250"> <img src="https://github.com/hy0417sage/study-git/blob/main/honux-git.jpg" height="250">

***

## Git을 배워야 하는 이유!
- Git은 VCS(Version Control System)란 종류의 프로그램들 중 하나이다. 
- 프로그램의 버전 관리를 위한 툴이다.
    - 프로그램의 버전 : 유의미한 결과가 결과물로 나온 것

## 버전을 관리한다는 것은? 
- 프로젝트의 시간과 차원을 관리하는 것이다.
- 개발자들이 프로그래밍을 하면서 필요에 따라 **시간여행**을 하고 **여러 차원을 넘나들 수** 있게 해준다. 
1. 시간
```
ver1 - ver2 - ver3 - ver4 - ver5 이렇게 프로젝트를 진행하고 있을 시 ver2에서 오류가 생긴다면? 
ver2의 오류를 수정할 수 있다.
```
2. 차원
```
메인 프로젝트를 망치지 않으면서 다양한 아이디어를 시도할 수 있다.
프로젝트의 내용들을, 마치 다른 폴더 인것 처럼 여러 모드로 자유롭게 전환하고 변경사항들을 쉽게 이동할 수 있다.
```

## CLI(Command Line Interface) vs GUI(Graphical User Interface)
- CLI : 명령줄을 입력해서 사용하는 인터페이스 (터미널, Git Bush 등이 있다.)
- GUI : 일반인 사용자들이 쓰기 편하도록 그래픽 요소를 활용한 인터페이스 (소스트리를 설치해서 사용할 수 있다.)
- git에서 뭔가를 실행하기 위한 어떤 명령들을 사용할 때는 CLI를 사용하고 프로젝트의 상태를 git창에서 자세히 살펴보아야 할 때는 GUI를 사용한다. 
- 혼용해서 사용하면 좋다.

## 1. Git 최초 설정
- 동료들과 협업할 때 어떤 작업들을 누가 했고 어떻게 연락할 수 있는지를 알기 위해 설정한다.
```git
git config --global user.name "이름"
git comfig --global user.email "이메일"
```
- 기본 브랜치명 변경
    - 기존에 사용하던 master 브랜치는 옛날 흑인 노예들을 연상시키는 단어라 main으로 변경!
```git
    git config --global init.defaultBranch main
```

## 2. 프로젝트 생성 & Git 관리 시작
- .git 생성
```git
git init
```
- 현재 폴더에서 현재 폴더의 상황을 git의 관점에서 보여줌
```git
git status
```
