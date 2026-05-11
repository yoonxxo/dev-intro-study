# 4주차

## Git Stage
:Git이 버전관리 하는 법

1. 코드를 수정한다. 저장할지 아닌지 모르는 상태
2. git add: commit에 넣을 후보로 올려두기="staging area에 올린다." stage는 commit 직전의 임시공간을 말한다.
3. git commit/push: 출판하기

- .git 폴더(숨김 폴더) 보는 법
    1. (windows) 파일 탐색기 상단 [보기]->[표시]->[숨김항목] 체크
    2. .git/objects폴더에 commit id와 일치하는 파일을 찾을 수 있다.
모든 commit은 코드 전체를 정리해서 보관하는데, 이를 snapshot이라고 한다. 즉, 코드가 바뀌면 바뀐부분만 저장하는 것이 아니라 **전체를 다시 압축해서 저장**한다.

## branch 충돌
main에서 새로운 branch를 파고 작업할 때, main의 코드와 branch에서 작업한 코드가 충돌이 일어나면, PR을 시도 했을 때 오류가 발생한다. 이때 Resolve conflicts과정이 필요하다.
```
<<<develop(새로 판 branch)
코드
===
코드
>>> main
```
새로 판 branch의 코드와 main의 코드 중 하나를 선택한다. Mark as resolved -> Commit merge 하면 충돌이 해결되고, PR이 가능해진다.

## Convention
협업 시, commit message는 작성한 코드의 목적이나 기능을 잘 나타내도록 작성하여야 한다. 그래야 개발자들 사이의 소통이 원활해지기 때문이다. 이에 관련하여 팀 프로젝트마다, 레포지토리 마다 정해놓은 룰이 Convention이다.

- branch명, PR명, commit은 같은 흐름으로 간다.
- 코드수정 비용이 적게 든다.

### Git Flow와 Github Flow
- Git Flow (branch 이름 짓는 방식): 역할 여러개로 나눠서 체계적으로 관리한다.
    - main: 배포용 코드
    - develop: 개발 중인 코드 
    - feture/기능 설명
    - fix/고친 설명 (develop에서)
    - ghotfix/고친 설명 (main에서)

- Github Flow
    - feature/기능 설명 한종류 뿐이다. (임시 작업실 느낌. 작업끝나면 없앰)

### Commit Convention
: 커밋 메세지 규칙
`type(scope): message`  (scope는 선택사항)

feat: 기능 추가
fix: 버그 수정
docs: 문서 수정
style: 스타일만 변경
refactor: 기능 변화없이 코드 개선
test: 테스트 코드
chore: 기타

### PR 템플릿
: PR할 때 자동으로 뜨는 작성양식

Github repo에 다음 파일을 만들면 된다.
.github/pull_request_template.md

