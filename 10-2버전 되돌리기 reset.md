# 버전 되돌리기 reset

## 기능 reset 이해
### 커밋 이력에서 이전 특정 커밋으로 완전히 되돌아가는(roll back) 방법
- 깃 저장소는 이전 커밋 내용으로 수정

## 버전 되돌리기 reset 전에 수행
-  현재의 작업 디렉토리와 스테이징 영역을 임시 저장에 저장
    -  $ git stash 
- 확인
    - $ git stash list
- 현재 상태 확인
    - $ git status

## reset 옵션 --hard
### $ git reset --hard HEAD~
- 지정된 HEAD~의 내용으로 작업 폴더와 스테이지 영역, 깃 저장소가 모두 복사・수정

## reset 옵션 --mixed
###  git reset --mixed HEAD~
- 지정된 HEAD~의 내용으로 스테이지 영역과 깃 저장소가 모두 복사, 수정

## reset 옵션 soft
### $ git reset --soft HEAD~
- 지정된 HEAD~의 내용으로 깃 저장소만 복사・수정

## 다시 원래 상태로 복원
### reset 이전의 커밋 ID를 ORIG_HEAD에 저장
- $ git reset --hard ORIG_HEAD

## 작업 디렉토리와 스테이징 영역 수정
- $ git stash apply --index

## reset과 checkout 비교
### $ git reset 9033
- 브랜치의 마지막 커밋을 수정하는 명령

### $ git checkout 9033
- HEAD 포인터를 브랜치 마지막 커밋 이전으로 이동하는 명령

## checkout으로 과거 여행 복습
### 상태가 깔끔해야 checkout 가능
- Nothing to commit, working tree clean
