### commit
```
git commit
```
Vi 입력 모드로 진입
|작업|vi명령어|상세|
|---|---|---|
|입력 시작|i|명령어 입력 모드에서 텍스트 입력 모드로 전환|
|입력 종료|esc|텍스트 입력 모드에서 명령어 입력 모드로 전환|
|저장 없이 종료|:q||
|저장 없이 강제종료|:q!|입력한 것이 있을 때 사용|
|저장 하고 종료|:wq|입력한 것이 있을 때 사용|
|위로 스크롤|k||
|아래로 스크롤|j||
> 마우스가 없던 시절 키보드 단축키로만 코딩하던 시절 사용하던 에디터

커밋 메시지까지 함께 작성하기
```
git commit -m "FIRST COMMIT"
```

add와 commit 한꺼번에
```
git commit -am "(메시지)"
```
>새로 추가된(untracked) 파일이 없을 때 한정


---
### Git에서 과거로 돌아가는 두 방식
* reset : 원하는 시점으로 돌아간 뒤 이후 내역들을 지운다
* revert : 되돌리기 원하는 시점의 커밋을 거꾸로 실행한다

**reset 사용해서 과거로 돌아가기**
```
git reset --hard (돌아갈 커밋 해시)
```
> 뒤에 커밋 해시가 없으면 마지막 커밋을 가리킴

**revert 로 과거의 커밋 되돌리기**
```
git revert (되돌릴 커밋 해시)
```
**커밋해버리지 않고 revert하기**
```
git revert --no-commit (되돌릴  커밋 해시)
```
> 원하는 다른 작업을 추가한 다음 함께 커밋

> 취소하려면 git reset --hard


### reflog 명령어

`reset`으로 사라진 커밋을 복구할 수 있는 `reflog` 명령어
```
git reflog
```
> `reflog`는 프로젝트가 위치한 커밋이 바뀔 때마다 기록되는 내역을 보여주고
이를 사용하여 `reset`하기 이전 시점으로 프로젝트를 복구할 수 있다

---

### Reference

[인프런 얄코님의 git강의](https://www.inflearn.com/course/%EC%A0%9C%EB%8C%80%EB%A1%9C-%ED%8C%8C%EB%8A%94-%EA%B9%83/dashboard)
