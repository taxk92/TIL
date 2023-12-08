![three2](https://github.com/taxk92/TIL/assets/135501581/55a2bc8d-47c5-4ead-a67c-7f9f4d054dde)
> commit되어 레포지토리에 들어간 후 수정사항이 발생하면 tracked 파일로써 스테이징을 기다리게 된다

### Working directory
* untracked: Add된 적 없는 파일, ignore 된 파일
* tracked: Add된 적 있고 변경내역이 있는 파일
* `git add` 명령어로 Staging area로 이동

### Staging area
* 커밋을 위한 준비 단계
* `git commit` 명령어로 repository로 이동

### Repository
* 커밋된 상태

---
### 파일을 `staging area`에서 `working directory`로
```
git restore --staged (파일명)
```
> `--staged`를 빼면 `working directory`에서도 제거

### reset의 세 가지 옵션
* --soft: `repository`에서 `staging area`로 이동
* --mixed (default): `repository`에서 `working directory`로 이동
* --hard: 수정사항 완전히 삭제

---

### Reference
[인프런 얄코님의 git강의](https://www.inflearn.com/course/%EC%A0%9C%EB%8C%80%EB%A1%9C-%ED%8C%8C%EB%8A%94-%EA%B9%83/dashboard)
