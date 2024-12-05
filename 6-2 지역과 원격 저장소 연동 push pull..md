# 개인접근토큰(Personal Access Token) 생성
## Personal Access Tokens
- 1.프로필 메뉴   
    로그인 후 GitHub.com에서 우측 메뉴 Settings
- 2.프로파일 settings 메뉴   
    왼쪽 메뉴 가장 하단: Developers settings
- 3.Personal access tokens  
    Generate new token,  암호 인증
- 4.값 입력   
    Generate token,
    범위 선택
## 깃 깃허브 push pull
- 올리고 내린다.

## 원격 저장소 수정 후 지역 저장소에서 pull
- 깃허브 원격 저장소에서 수정 후 커밋
원격 저장소의 수정을 지역 저장소에 반영
    - 지역 저장소에서 pull

# 지역에서 원격 저장소로 push

## 지역 저장소에서 push
- 쓰기 권한이 있어야 push가 가능
    - 자신의 저장소나 다른 사람의 저장소라면 협업자(collaborator)로 등록
- Push
    -  로컬 저장소에서 남겨놓은 코드 변경  이력들이 원격 저장소로 전송
- 명령
    - $ git push <저장소별칭명> <브랜치명>
    - $ git push origin topic

## 명령 push에서 인자 생략하기
- 옵션 –u 사용(최초 한번으로 이후 생력 가능)
    - $ git push origin topic
    - $ git push
- 항상 현재 브랜치를 기준으로 작동
    - $ git config --global push.default current로 설정
    - $ git push

## git pull = git fetch + git merge
- git pull 명령
    - fetch 명령과 병합하는 merge 명령이 순차적으로 진행
- fetch 명령
    - 원격 저장소의 정보를 로컬(remote/origin) 저장소로 가져오는 명령
    - $ git fetch <remote>
    -  $ git fetch origin
- merge 명령
    - 변경된 정보를 로컬 저장소의 내용과 병합

## fetch 후 병합
- 깃허브의 내용을 반영하려면 fetch 후 merge 해야함
    - $ git merge origin/main

## 지역에서 원격 저장소로 push
###  원격을 포함한 모든 브랜치 파악
- 지역의 브랜치와 HEAD
    - main HEAD
- 원격의 브랜치와 HEAD
    - origin/main origin/HEAD
