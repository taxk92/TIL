### 로컬에 원격 저장소 추가 후 푸시
>  HTTPS 프로토콜 사용

GitHub 레포지토리 생성 후
```
git remote add origin (원격 저장소 주소)
```
> 로컬의 Git 저장소에 원격 저장소로의 연결 추가
>
>원격 저장소 이름에 흔히 origin 사용. 다른 것으로 수정 가능


```
git branch -M main
```
> GitHub 권장 - 기본 브랜치명을 main으로

```
git push -u origin main
```
> 로컬 저장소의 커밋 내역들 원격으로 push(업로드)
> 
> -u 또는 --set-upstream : 현재 브랜치와 명시된 원격 브랜치 기본 연결

원격 목록 보기
```
git remote
```

### GitHub에서 프로젝트 다운받기
* Download ZIP: 파일들만 다운받음, Git 관리내역 제외

* Git clone: Git 관리내역 포함 다운로드

터미널이나 Git Bash에서 대상 폴더 이동 후
```
git clone (원격 저장소 주소)
```

### 원격으로 커밋 밀어올리기(push)
```
git push
```

### 원격의 커밋 당겨오기(pull)
```
git pull
```

### pull 할 것이 있을 때 push를 하면?
* 원격에 먼저 적용된 새 버전이 있으므로 push 불가

* pull 해서 원격의 버전을 받아온 다음 push 가능

**push 할 것이 있을 시 pull 하는 두 가지 방법**

1. *git pull --no-rebase* - merge 방식

2. *git pull --rebase* - rebase 방식


### 로컬에서 브랜치 만들어 원격에 push 해보기

1. from-local 브랜치 만들기
2. 아래 명령어로 원격에 push
```
git push -u origin from-local
```

아래 명령어로 로컬과 원격의 브랜치들 확인
```
git branch --all
```

### 원격의 브랜치 로컬에 받아오기
1. GitHub에서 from-remote 브랜치 만들기
2. 아래 명령어로 원격의 변경사항 확인
```
git fetch
```
3. 아래 명령어로 로컬에 같은 이름의 브랜치를 생성하여 연결하고 switch
```
git switch -t origin/from-remote
```

### Reference
[인프런 얄코님의 git강의](https://www.inflearn.com/course/%EC%A0%9C%EB%8C%80%EB%A1%9C-%ED%8C%8C%EB%8A%94-%EA%B9%83/dashboard)
