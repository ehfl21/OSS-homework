# 파일비교diff

## 파일비교diff 명령어 요약

| 명령어                         | 설명                                     |
|--------------------------------|------------------------------------------|
| `$ git diff`                   | 스테이징 영역 기준으로 작업 디렉토리 파일 비교            |
| `$ git diff --staged HEAD `               | 깃 저장소 기준으로 스테이징 영역 파일 비교 |
| `$ git diff HEAD`      | 깃 저장소 기준으로 작업 디렉토리 파일 비교            |

# 파일삭제rm과복구restore

## 명령 별칭(git alias) 생성
### 계속 사용하는 깃 명령을 짧게 다른 이름으로 만드는 방법
$ git 별칭이름
$ git config --global alias.별칭이름 ‘원명령어 --긴옵션 -짧은옵션’
> 설정 이후에는 다음 명령으로 가능
- 예: $ git config --global alias.ss 'status -s‘
### 다음은 동일한 명령어
```bash
$ git status –s
$ git ss
$ git config --global alias.s status
$ git s
$ git config --global alias.co checkout
$ git co
$ git config --global alias.br branch
$ git br
```
- -- global은 모든 프로젝트에서
공통적으로 사용하고자 하는 설정

## 사용자의 홈디렉토리의 .gitconfig파일에 아래와 같이 추가
```bash
[alias]
ss = status –s
s = status
co = checkout
br = branch
c = commit
$ git config --global alias.c commit
$ git c
```