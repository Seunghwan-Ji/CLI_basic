# CLI(Command Line Interface) basic (Unix Commands)

## git bash

### 기본 조작
- `$`: 프롬프트 ==> 현재 명령어를 받을 준비가 되었다 + 터미널 명령어다.
- `ctrl + c`: 취소 ==> Cancel
- `ctrl + l`: 클리어 ==> clear
- `↑ ↓`: 기존 명령어 불러오기
- `tab`: 자동 완성

### 명령어들
- `touch`: 파일 생성
- `ls`: 현재 폴더의 내용물을 보여줌(list)
- `ls -a`: 현재 폴더의 내용물을 모두 보여줌(all)
- `rm`: 파일 삭제(remove)
- `rm -r`: 파일/폴더 모두 삭제(recursively)
- `rm -rf`: 파일/폴더 모두 강제 삭제(force)
- `pwd`: 현재 작업 폴더 = 내위치(Present Working Directory)
- `mkdir`: 폴더 생성(nake directory)
- `rmdir`: 빈 폴더 삭제(remove directory)
- `cd`: 폴더 이동(change directory)
- `cp`: 파일 복사(copy)
- `cp -r`: 파일/폴더 복사
- `mv`: 파일/폴더 이동 + 이름 바꾸기

### 경로 관련
- `.`: 현재 폴더
- `..`: 상위 폴더
- `~`: home dir
- `/`: root dir
- `.xxx`: `.` 으로 시작 => 숨김 파일/폴더

## git 기초

### 개념
- VCS(Version Control System)
- Git vs Github
- Open source
- Git
  - Working Directory 
  - Stage
  - Commit

### 명령어
```
$ git init (Master 부여)
$ git config --global user.name 'NAME' (유저네임 등록)
$ git config --global user.email 'EMAIL' (이메일 등록)
$ git add <file> (파일 스테이징)
$ git add . (모든 파일 스테이징)
$ git commit -m 'MESSAGE' (스테이징한 파일 커밋)
$ git remote add origin 'URL' (자신의 github 원격 저장소를 연결합니다.)
$ git push origin master (자신의 github로 파일을 푸쉬(파일 추가 or 업데이트)합니다.)
$ git clone 'URL' (현재 터미널에서 해당 URL의 파일들을 복제하여 저장합니다.)
$ git branch <branch-name>
$ git switch <branch-name>
$ git branch -d <branch-name>
$ git merge <target-branch>
$ git branch
$ git branch -d
$ git branch -D
$ git switch
$ git switch -c
$ git merge
$ git log --oneline --graph
$ git pull origin master (원격 저장소의 변경사항을 가져옵니다.)
$ git pull origin master --allow-unrelated-histories
$ git push --force origin master (강제로 푸쉬합니다.)
<모든 커밋에서 삭제>(주로 커밋된 용량 큰 파일 삭제용)
$ git filter-branch --force --index-filter "git rm --cached --ignore-unmatch path/file.mp4" --prune-empty --tag-name-filter cat -- --all
$ git push origin --force --all
$ git push origin --force --tags
```

#### git 최초 등록
```
$ git init
$ git config --global user.name 'NAME'
$ git config --global user.email 'EMAIL'
```

#### 새로운 마크다운 파일 생성 -> 스테이징(add) -> 커밋

##### 비유: 분장실 -> 광고 촬영장 -> 촬영 후 촬영물 저장
```
$ git touch file.md (분장실에서 사람이 대기합니다.)
$ git add file.md (사람이 촬영장에 들어옵니다.)
$ git commit m- "message" (촬영 후 영상을 저장합니다.)
```
##### 위와 같이 파일 생성 후 커밋을 하기전에 반드시 스테이징이 이루어져야 합니다.

#### 모든 파일 한번에 스테이징
```
$ git add .
```

#### 기록 확인
```
$ git status
$ git log
$ git log --oneline (한 줄씩 보여줍니다.)
```

## 일반적인 github를 활용한 프로젝트 진행 절차
1. 프로젝트 파일 생성
2. git init
3. 파일 생성 및 최초 커밋 진행(git touch, git add ., git commit -m "")
4. 원격 저장소 연결(git remote add origin "URL")
5. 프로젝트 진행
6. git add file.md
7. git commit -m "message"
8. 5번으로 돌아감
9. 필요할 때 Push(git push origin master)

## 반드시 파일명은 .gitignore

### 프로젝트 생성시 README.md / .gitignore 는 반드시 먼저 생성 하고 커밋하자.

## 강사님 이메일: verba.it.corp@gmail.com