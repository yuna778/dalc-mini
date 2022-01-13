# git - VCS(Version Control System)
: 파일의 변화를 기록하고 저장하는 시스템
- 소스 코드의 변경 사항 추적
- 특정 코드의 개발자 및 개발 목정 기록
- 버전 관리
- 오류 복구, 이전 버전으로 복구
- 기존 버전에 영향을 주지 않으면서 신규 개발 및 수정 작업을 진행
- 개발 요건 및 버전간 영향을 주지 않으면서 독립적인 개발을 진행
- 개발자간 소스코드 동기화

* 초기 설정
```
git config --global user.name "dalc"
git config --global user.email dalc@gmail.com
```

* 저장소 클론하기
```
git clone <저장소 주소>
```

* 저장소 만들기
```
git init
git remote add origin <저장소 주소>
```


## commit하기
* 특정 버전을 저장하는 것 = commit 한다
    - 특정 버전 = commit
        - Working Directory : 프로젝트 디렉토리 자체
        - Staging Area : 특정 버전으로 관리하고 싶은 파일들을 모아두는 장소
        - Repository : 특정 시점의 staging area의 모습을 commit으로 남기면 commit들이 저장되는 영역

### commit 간 이동
- HEAD : 현재 내가 위치해있는 커밋을 가리키는 식별자
- HEAD를 바꾸면 HEAD가 가리키는 commit으로 working directory의 모습 변화

```
git reset -- {option} {commit_id}
```
||HEAD바뀜|WD변화|SA변화
|------|-------|-------|------|
|Hard|o|o|o|
|Mixed|o|x|o|
|Soft|o|x|x|
