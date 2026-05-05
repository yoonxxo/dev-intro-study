# 3주차
## branch 만들기
- git: 컴퓨터에 있는 프로젝트(repository)
- github: git을 관리하는 플랫폼

"코드를 변경하고 commit을 하면 (vercel로) 배포한 URL에도 적용된다.
이때, 잘못된 코드를 commit 해버리면 홈페이지에는 404 not found가 뜬다.
이를 방지하기 위한 것이 branch."

- branch(분기)란?
    : main이 되는 배포된 코드와 개발용 코드를 분리하여, 개발용 코드에서 작업 후 main에 합친다.

- branch 이름
    - main: 배포용 코드
    - develop: 개발 중인 코드 
    - feture/기능 설명
    - fix/고친 설명 

- branch 만들기
    : Github desktop-Create a Branch-branch 이름 입력 후 생성

- branch 합치기
    1. 작성한 코드를 develop에 commit
    2. Pull Request (PR): 브랜치를 main에 merge할 것을 요청한다.

## css
CSS란?
Cascading Style Sheets.
Cascading: 우선순위를 가진다. 계단식이다.
Style Sheet: CSS의 스타일 규칙들을 모아둔 파일이나 블록
-> Style Sheet의 규칙들을 따르며, 계단식인 스타일 지정 문법

- 인라인(inline) 스타일 방식: 태그에 직접 스타일을 입히는 방식

- 내부 스타일 방식: "파일 내"의 태그들에 style을 한번에 적용 (head 태그 내에 정의)
    ```html
    <style>
    h1, h2, h3, h4, h5, h6 {
    color: yellow;
    background-color: red;
    }
    </style>
    ```

- 외부 스타일 방식: HTML 문서와는 별개의 파일(style.css)에서 스타일을 지정하는 방법. 스타일을 한 번에 작성해서 여러 HTML 문서에 적용할 수 있어 유지보수에 용이하다. 

    ```css
    h1, h2, h3, h4, h5, h6
    { color: red; background-color: yellow; }
    ```
    
    <html과 style.css 파일 연결하기>
    ```html
    <link rel="stylesheet" href="./style.css">
    ```
    
- **우선순위**: 인라인> 내부 >외부

- 색상을 정의하는 방법
    - RGB: rgb함수에 red, green, blue 값을 0 - 255 스케일로 정의 Ex) `color: rgb(255, 0, 0);`
    - HEX CODE: 두 자리 단위로 끊어서, red, green, blue 값을 16진수로 정의 `background-color: #FFFF00;`

- class
    : 원하는 태그만 분류해서 스타일을 동시에 적용한다.
    ```css
    .zzang { //zzang이라는 class 생성
    color: red;
    background-color: yellow;
    }
    ```
    
    ```html
    <body>
    <h1 class="zzang">신짱구</h1> //h1태그에 zzang 클래스 스타일 적용
    <p>안녕하세요. 저는 떡잎마을에 사는 <span class="zzang">신짱구</span>입니다. 5살이에요.</p> //신짱구 글씨에 zzang 클래스 스타일 적용
    ...
    <body>
        ```

## Margin과 Padding
- margin: 요소 바깥쪽 공간. 바깥 여백
    - 속성 4개(위, 오른쪽, 아래 왼쪽) 사용 시: `margin: 10px 5px 10px 5px;`
    - 속성 2개 사용 시 위아래/ 오왼 여백 의미: `margin: 10px 5px;`
    - 속성 1개 사용 시 모든 방향이 같은값을 사용한다.
    - 가운데 정렬 `margin: 0 auto;`
    
- padding: 내용과 테두리 사이 거리. 내부 여백
    - 속성 1개 사용 시 안쪽 여백이 변경된다. `padding: 20px;`

    - 한 방향에만 값을 부여하고 싶은 경우: `margin-right: 20px, padding-top: 10px;`
