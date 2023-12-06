## Git 최초 설정

### Git 전역으로 사용자 이름과 이메일 주소를 설정
* GitHub 계정과는 별개

터미널 프로그램 (Git Bash, iTerm2)에서 아래 명령어 실행
```
git config --global user.name "(본인 이름)"
```
```
git config --global user.email "(본인 이메일)"
```

아래의 명령어들로 확인
```
git config --global user.name
```
```
git config --global user.email
```

### 기본 브랜치명 변경
```
git config --global init.defaultBranch main
```
> 기존 master 라는 브랜치명은 인종차별적 느낌이라 main 으로 바꾼다고 한다

---
##  프로젝트 생성 & Git 관리 시작
적당한 위치에 원하는 이름으로 폴더를 생성하고 VS Code로 열람

해당 폴더에서(VS Code 터미널 기본) 아래 명령어 입력
```
git init
```
폴더에 숨김모드로 .git 폴더 생성 확인
> 이 폴더를 지우면 Git 관리내역이 삭제된다 (현 파일들은 유지)

### Git의 관리에서 특정 파일/폴더를 배제해야 할 경우

* 포함할 필요가 없을 때
  
자동으로 생성 또는 다운로드되는 파일들 (빌드 결과물, 라이브러리)
* 포함하지 말아야 할 때

보안상 민감한 정보를 담은 파일

**.gitignore 파일을 사용해서 배제할 요소들을 지정할 수 있다.**

---

### Reference
[인프런 얄코님의 git강의](https://www.inflearn.com/course/%EC%A0%9C%EB%8C%80%EB%A1%9C-%ED%8C%8C%EB%8A%94-%EA%B9%83/dashboard)
