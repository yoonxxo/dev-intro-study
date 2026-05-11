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