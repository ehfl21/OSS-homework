# 깃 4 영역과 임시 저장 개요

## Git Stash
- 커밋할 필요 없이 파일의 변경 사항을 숨기거나 비밀리에 저장할 수 있는 강력한 도구
- 따로 안전한 곳에 저장했다가 다시 가져올 수 있는 기능

### 브랜치 이동 또는 이전 커밋으로 이동
- $ git switch bname
- $ git checkout HEAD~

# 임시 저장 명령 stash

## 작업 폴더와 스테이징 영역을 숨김(stash)에 저장하고 작업 폴더를 정리
- $ git stash
- $ git stash –m ‘메시지’
- $ git stash save
- $ git stash save ‘메시지’

### 작업 디렉토리 내용만 다시 복사
- $ git stash apply
### 스테이지 영역도 함께 복사
- $ git stash apply --index

## 주요 명령어
| 명령어                                  | 설명                                     |
|-----------------------------------------|------------------------------------------|
| `옵션 –k : --keep-index`                   |스테이징 영역은 저장하지 않고 그대로 놔둠, checkout 불가 |
| `옵션 –u: --include-untracked`                   |Untracked 파일도 포함해 저장|`           |
| `옵션 –p: --patch `     | 대화형 프롬프트를 통해자신이 stash에 저장할 것과 저장하지 않을 것을 지정 가능
   |
```bash
$ git stash list
stash@{n}
```
- Stash 목록 볼수있음

```bash
$ git stash show
```
- 변화된 파일과 변화된 수만 표시

```bash
$ git stash show –p
```
- -p: 파일 내용의 차이까지 보이기

| 명령어                                  | 설명                                     |
|-----------------------------------------|------------------------------------------|
| `$ git stash pop`                   |최근 또는 지정된 임시저장소 내용을 가져와 반영하고 삭제 |
| `$ git stash apply`                   |최근 또는 지정된 임시저장소 내용을 가져와 반영, 작업 디렉토리만 반영,stash 목록은 그대로|`           |
| `$ git stash apply --index `     | 최근 또는 지정된 임시저장소 내용을 가져와 반영, 작업 디렉토리와스테이징 영역도 반영, stash 목록은 그대로
   |
| `$ git stash drop`  | 최근 임시저장 내용을 삭제 |
| `$ git stash drop stash@{n}`               | 지정된 임시저장 내용을 삭제|
| `$ git stash clear `      | 모든 stash 목록을 모두 제거           |