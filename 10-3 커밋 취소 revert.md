# 커밋 취소 revert

## 커밋 취소 revert 
- 지정한 특정 커밋을 취소해 바로 이전 상태로 되돌리는 방법

## 명령 revert
### 옵션 --no-edit
- git revert HEAD~
- git revert HEAD~ --no-edit

## 오류가 발생해 revert가 취소
### 해결 방법
- git reset --hard HEAD~
### 바로 전 revert 취소
- $ git reset --hard HEAD~
### 기본 편집기로 새로운 취소 메시지 편집 후 저장, 닫기
- $ git revert HEAD

# reset vs revert 비교

## reset vs revert
### 되돌리기, 재설정 reset
- 특정 커밋으로 되돌아가고 그 이후의 로그 이력은 모두 제거
### 커밋 취소 revert
- 특정 커밋을 취소하는 새로운 커밋 생성, 이전 모든 이력은 그대로 남음