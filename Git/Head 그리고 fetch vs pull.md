![heads](https://github.com/taxk92/TIL/assets/135501581/2ec5d4ad-196a-49e0-a72c-b45b9fed0b63)

### Git의 Head
현재 속한 브랜치의 가장 최신 커밋

### `checkout`으로 앞뒤 이동해보기
```
git checkout HEAD^
```
* `^` 또는 `~`: 갯수만큼 이전으로 이동
  * `git checkout HEAD^^^`, `git checkout HEAD~5`
* 커밋 해시를 사용해서도 이동 가능
  * `git checkout (커밋해시)`
 
---

### `fetch`와 `pull`의 차이
* `fetch`: 원격 저장소의 최신 커밋을 로컬로 가져오기만 함
* `pull`: 원격 저장소의 최신 커밋을 로컬로 가져와 `merge` 또는 `rebase`

---

### Reference
[인프런 얄코님의 git강의](https://www.inflearn.com/course/%EC%A0%9C%EB%8C%80%EB%A1%9C-%ED%8C%8C%EB%8A%94-%EA%B9%83/dashboard)
