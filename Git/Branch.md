![branches](https://github.com/taxk92/TIL/assets/135501581/7c662cc7-6ac2-4ee9-8fd6-26af3137d7f9)

### Branch : 분기된 가지
* 프로젝트를 하나 이상의 모습으로 관리해야 할 때
  * 예) 실배포용, 테스트서버용, 새로운 시도용
* 여러 작업들이 각각 독립되어 진행될 때
  * 예) 신기능 1, 신기능 2, 코드개선, 긴급수정...
  * 각각의 차원에서 작업한 뒤 확정된 것을 메인 차원에 통합


### 브랜치 생성 / 이동 / 삭제하기
add-coach란 이름의 브랜치 생성
```
git branch add-coach
```
브랜치 목록 확인
```
git branch
```
add-coach 브랜치로 이동
```
git switch add-coach
```
브랜치 생성과 동시에 이동하기
```
git switch -c (브랜치이름)
```
브랜치 삭제하기
```
git branch -d (삭제할 브랜치명)
```
브랜치 이름 바꾸기
```
git branch -m (기존 브랜치명) (새 브랜치명)
```

---

### 서로 다른 브랜치를 합치는 두 방식
* merge : 두 브랜치를 한 커밋에 이어붙인다
  * 브랜치 사용내역을 남길 필요가 있을 때 적합한 방식
* rebase : 브랜치를 다른 브랜치에 이어붙인다
  * 한 줄로 깔끔히 정리된 내역을 유지하기 원할 때 적합

**add-coach 브랜치를 main 브랜치로 merge**
* main 브랜치로 이동
```
git merge add-coach
```

**rebase로 합치기**
add-coach 브랜치를 main 브랜치로 rebase
* add-coach 브랜치로 이동
  > merge 때와는 반대!
```
git rebase main
```
> main 브랜치는 뒤쳐져 있는 상황 (소스트리같은 gui에서 확인해보면)

main 브랜치로 이동 후 아래 명령어로 add-coach의 시점으로 merge
```
git merge add-coach
```

**브랜치 간 충돌**

파일의 같은 위치에 다른 내용이 입력된 상황

vscode에서 해당 부분 확인 후

당장 충돌 해결이 어려울 경우 아래 명령어로 중단
```
git merge --abort
```
```
git rebase --abort
```

해결 가능 시 충돌 부분을 수정한 뒤 git add .

아래 명령어로 계속
```
git rebase --continue
```

---
## 다른 브랜치의 원하는 커밋 가져오기
`cherry-pick` 명령어 사용

### 다른 브랜치 커밋 main 브랜치로 가져오기
main 브랜치에서 실행
```
git cherry-pick (다른 브랜치 커밋 해시)
```

---
## 다른 커밋들을 하나로 묶어 가져오기
merge --squash 옵션 사용

### 다른 브랜치의 마디들을 하나로 묶어 main 브랜치로 가져오기
```
git merge --squash (대상 브랜치)
```
* 변경사항들 스테이지 되어 있음

* `git commit` 후 메시지 입력

> 일반 merge와의 차이 정리
>
> 일반 merge와 merge --squash는, 실행 후 코드의 상태는 같지만
> 내역 면에서 큰 차이가 있는 것이라고 이해
> * 일반 merge : A와 B 두 브랜치를 한 곳으로 이어붙임
> * merge --squash : B 브랜치의 마디들을 복사해다가 한 마디로 모아 A 브랜치에 붙임 (staged 상태로)


---
## Gitflow
협업을 위한 브랜칭 전략

![git-model@2x](https://github.com/taxk92/TIL/assets/135501581/be50311f-9375-488b-959b-26d3bdd96fef)

### 사용되는 브랜치들
|브랜치|용도|
|--|--|
|main|제품 출시/배포|
|develop|다음 출시/배포를 위한 개발 진행|
|release|출시/배포 전 테스트 진행(QA)|
|feature|기능 개발|
|hotfix|긴급한 버그 수정|

---

### Reference
[인프런 얄코님의 git강의](https://www.inflearn.com/course/%EC%A0%9C%EB%8C%80%EB%A1%9C-%ED%8C%8C%EB%8A%94-%EA%B9%83/dashboard)
