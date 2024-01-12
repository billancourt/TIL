# Git
분산형 버전 관리 시스템

코드의 버전(history)이 관리·개발되어온 과정 파악

이전 버전과의 변경 사항 비교

### Git의 3가지 영역
1. Working Directory 
2. Staging Area
3. Repository

### Git 명령어
> git init : git initialize, 로컬 저장소 설정(초기화)

> git add : Working Directory에서 변경 사항이 있는 파일을 Staging Area에 추가
  >> git add . : 같은 Working Directory 내 여러 파일들을 한번에 전부 Staging Area에 추가

> git commit -m "" : Staging Area에 있는 파일들을 저장소에 기록, 해당 시점의 버전을 생성하고 변경 이력을 남기는 것

> git status : git의 현재 상태 확인

> git log : git의 commit history 조회
  >> git log --oneline : git log를 한 줄로 조회

> git config : git에서의 username, email 등의 설정 기능
  >> git config --global -l : git global 설정 정보 조회

> git remote add origin remote_repo_url : 로컬 저장소에 원격 저장소 주소 추가(이때 origin은 원격 저장소의 별칭이며 수정 가능)

> git push -u origin master : 원격 저장소에 commit 목록을 업로드 

> git pull origin master : 원격 저장소의 변경 사항만을 다운로드

> git clone remote_repo_url : 원격 저장소 전체를 다운로드(복제)

> git remote -v : 현재 로컬 저장소에 등록되어 있는 원격 저장소 목록

> git remote rm remote_repo_name(이 경우 origin) : 현재 로컬 저장소에 등록되어 있는 원격 저장소 삭제

### 주의사항
1. git 저장소 안에 또다른 git 저장소는 존재할 수 없음
   
   Desktop에서 git init 선언을 했을 때의 해결책 : git ls -a (all option) → 파일명이 . 으로 시작하는 숨김 파일을 찾아서 git rm -r file_name
2. git clone 이후 git init 선언 불필요
3. 로컬에서 변경해도 push하지 않으면 원격 저장소에는 저장되지 않음

### README.md
프로젝트에 대한 설명, 사용 방법, 문서화된 정보 등을 포함하는 역할

Markdown 형식으로 작성되며, 프로젝트의 사용자, 개발자, 혹은 기여자들에게 프로젝트에 대한 전반적인 이해와 활용 방법을 제공하는 데 사용

주로 프로젝트의 소개, 설치 및 설정 방법, 사용 예시, 라이선스 정보, 기여 방법 등을 포함  

***PLEASE NOTE***
> **반드시 저장소 최상단에 위치해야 원격 저장소에서 올바르게 출력됨**