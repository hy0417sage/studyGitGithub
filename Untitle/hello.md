## git 이란?
형상 관리 시스템(Verson Control System) 의 한 종류다. 
주로 개발자들이 프로그램과 관련된 파일들을 저장하는 데 사용한다.

# git 명령어 요약
- clone : 원격 저장소 복사
- add : 스테이지 영역에 작업 파일 추가
- commit : 세이브, 스테이지 영역의 파일들을 가지고 커밋(=세이브)를 만들 수 있음
- push : 원격 저장소에 커밋 업로드

# 파일의 내용 되돌리기(checkout)
- 특정 파일의 내용을 마지막 커밋으로 돌리고 싶다면 해당 파일 선택 후 '코드 뭉치 버리기' 선택

## 스파게티 코드를 막기 위한 방법
- 브랜치 (branch): 기능 변경을 하고 싶을 때 생성 및 사용
- 머지 (merge): 한 브랜치의 내용을 다른 브랜치에 반영
- 체크아웃 (checkout): 저장소에서 특정 커밋이나 브랜치로 돌아가고 싶을 때 사용, 여기서 헷갈리지 말자! ver2로 바꿔서 개발하고 싶다면 체크아웃하고 ver2로 가는거다. ($git chectout ver2)

## 브랜치
- 브랜치란? 가상의 작업 환경.
- 마스터 브랜치 : 사람들과 공유하고 싶은 최종 결과물이 있어야 하는 곳
- 헤드 브랜치 : 현제 작업중인 브런치, 현재 브런치라고도 한다.

## 새로운 브랜치 만들기
- 원하는 커밋을 만들고 우클릭, 새 브랜치 이름 입력하면 커밋으로 부터브랜치가 생긴다.

## 원하는 브랜치로 돌아가기
- checkout : 왼쪽의 브랜치 이름 입력하면 커밋으로부터 브랜치가 생긴다.

# 브랜치 변경하기
- 브랜치란 : 기존 내용을 유지한 채 새로운 내용을 추가하고 싶을 때 사용한다.
- 체크아웃 : 특정 브랜치(혹은 커밋)으로 돌아가고 싶을 때 사용.
- 소스트리 체크아웃 : 브랜치 이름을 더블 클릭하는 것만으로 체크아웃 가능.

## 병합(머지, merge)
- 하나의 브랜치를 현재 브랜치와 합치는 것
- git 시뮬레이션 가능한 사이트 : https://learngitbranching.js.org/

# 병합하기1
- 헤드 브랜치에 변경사항이 없고
- 병합 대상 브랜치가 해드로 부터 시작된 경우 아주 쉽게 병합 가능 (= fast-forword)

## 충돌
- 충돌은 자동 병합 실패시 발생
- 브랜치를 삭제했을 경우 사라지는 커밋이 있는지 없는지 확인하자.
- git pull 서버의 내용이 최신이 아닌경우 pull을 적용한다.
- 충돌이 날 수 있지만 놀라지 말자.
- pull = fetch + merge

## 충돌의 발생원인
- 자동 병합을 실패했을 경우 발생
- 주로 두 커밋이 같은 파일을 편집했을 경우 발생
- 충돌을 해결했는데 이상해 졌다면 reset시전

## reset으로 커밋 돌리기
- git reset --hard 에 해당하는 명령으로 커밋을 되돌리기
- reset이후 push는 force 옵션을 선택해야 함
- 이전 커밋을 사라짐
- push --force는 소스트리에서 지원하지 않기 때문에 CLI를 이용해야함

## reset의 장단점
- 장점 : 쉽다.
- 단점 : 커밋이 날아간다. push --force가 필요하다.
