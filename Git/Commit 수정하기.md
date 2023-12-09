## git commit --amend
마지막 커밋 수정

### 1. 커밋 메시지 변경
Commit 후 아래 명령어로 에디터 열어 커밋 메시지 변경
```
git commit --amend
```

### 2. 커밋에 변화 추가
* 파일 수정하거나 추가후 스테이지
* `git commit --amend`로 마지막 커밋에 포함

### 3. 커밋 메시지 한 줄로 변경
```
git commit --amend -m '(수정하고 싶은 커밋 메시지)'
```


---

## git rebase -i (대상 바로 이전 커밋)
과거 커밋 내역을 다양한 방법으로 수정 가능
|명령어|설명|
|--|--|
|p, pick|커밋 그대로 두기|
|r, reword|커밋 메시지 변경|
|e, edit|수정을 위해 정지|
|d, drop|커밋 삭제|
|s, squash|이전 커밋에 합치기|


---

### Reference
[인프런 얄코님의 git강의](https://www.inflearn.com/course/%EC%A0%9C%EB%8C%80%EB%A1%9C-%ED%8C%8C%EB%8A%94-%EA%B9%83/dashboard)
