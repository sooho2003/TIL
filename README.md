# TIL
## Vs code 주요 단축키
* `Ctrl + K` -> `Ctrl + \` 위/아래 수직 화면 분할
* `Ctrl + \` 좌/우 수평 화면 분할
* `Ctrl + J` 터미널 실행/닫기
* `Q` or `Ctrl + C` 터미널 입력 안되는 에러 해결
## 작업폴더 설명
* `html_bsic/`
* `task/` : 과제제출 폴더, 파일 모음(폴더명은 날짜별로 구성됨)
* `README.md` : 배운 내용 기록, 어려운 점 및 막힌 점 자유롭게 기록
### 2025/04/04 - HTML 3일차 문서와 레이아웃
* `h1~h6`, `p`, `br`, `strong`, `em`, `del`, `s`, `sup`, `sub`
* `h1~h6` 중 h1태그 구분이 어려움. 공부 필요함.`
* `2025/05/03` 네이버 프로젝트
* index.html 90번 line
### 2025/04/07 - HTML 4일차 레이아웃
* `div`, `span`
* `div`는 생성 시 반드시 그룹을 구분할 수 있는 이름을 설정해야 한다. `span`은 선택!
* 이름 작성 시 주의사항 : 반드시 용도에 맞는 의미있는 영단어 사용!!
### HTML 구조 공부 순서
1. 클론 코딩 & 클론 디자인할 사이트 정하기
2. 피그마에서 와이어프레임 만들기(레이어, 폴더 이름 주의)
3. 피그잼에 일부 화면 넘겨서 태그 계획하기
4. 계획한 태그를 가족관계에 맞게 트리구조 만들기
5. Vs code에서 실제 HTML 작성하기(트리구조 순서에 맞게 바깥쪽->안쪽순서로!)
### 다른 환경에서 git 이어서 작업하기
1. 새폴더 연결하기
2. `git clone 저장소주소붙여넣기`
3. `cd 저장소폴더명`
4. 자유롭게 수정 후 저장
5. `git status` 상태확인
6. `git add .` 스테이징 업로드
7. `git commit -m '메세지'`
8. `git push origin main` 저장소업로드
### (위 이어서) 다른 환경에서 git 이어서 작업하기(학원)
* `git pull origin main` 집에서 올린 파일 내려받기
### 바로가기 메뉴 만들기
0. (조건) 화면이 수직으로 충분히 이동할 수 있을만큼 세로 스크롤 준비
1. 바로가기 메뉴 a 태그 준비하기
2. 바로가기 위치 div id명 준비하기
3. 위 1번 `a` 속성 `href` 값으로 `#` 먼저 작성 후 위 2번 이름 작성하기
4. 위 3번 결과 예시) id가 abcd일 경우 `<a href="#abcd"></a>`
`<a(링크태그) href(주소를 담는 속성)="#"></a>`
`<a href="#header"></a>` - 임시링크(연결페이지 제작 전일 경우)
`<a href="./basic/index.html"></a>` - 바로가기링크(같은 파일 내 다른 위치 이동)
`<a href="./basic/index.html#main"></a>` - 상대경로링크+바로가기링크
----
## CSS Style sheet
* 외부스타일시트 파일 저장은 **styles**폴더에 `파일명.css` 저장한다.
* 위 파일 생성 후 CSS연결을 원하는 HRML파일 head위치에 `<link>`태그로 연결한다.
*HTML작성 후 HTML의 모든 디자인형태를 초기화하는 `reset.css` 반드시연결!
* 웹글꼴(Noto Sans KR, Pretendard 등) 연결 시 HTML파일에 `<link>`태그 연결!
### head태그 내에 들어가는 link태그 작성 순서
1. 웹글꼴 포함 기타 플러그인 연결 주소
2. reset.css
3. 해당 HTML별 디자인.css 
### 디자인 CSS 작성 시 작성 순서 및 주의사항
* **부모->자식**순서로 가장 바깥쪽 부모부터 먼저 선택자를 만들고 디자인한다.
* 레이아웃 관련 요소에 `width, height` 속성 작성 시 영역 확인을 위한 `background-color`를 꼭 함께 작성해서 정확히 구분한다. 이 때 색상은 쉬운 영역 구분을 위한 `aqua, lime, yellow, pink`등의 밝은 색상 위주로 사용한다. 영역 확인과  디자인 작업을 모두 마친 후 위 색상은 제거로 마무리해야한다.
* 실제 디자인에 들어가는 색상은 rgba 또는 헥사코드로 입력하고 테스트용으로 입력하는 임시 색상은 영문명으로 입력해야 한다.
### 자주 이용하는 CSS 속성 값 기본값
* `letter-height` 자간 | 기본값(0) | 사용예시(letter-spacing:-0.02rem;)
* `line-height` 선 | 글자가 두 줄 이상 있을 때 그 사이 = 행간 | 100% | line-height:1.5;
* `font-size` 글자 | 크기 |16px(1em) | `font-size:1.2rem;`
* `color` 색상 | `color:#f00; color:rgba(0,0,0,0.5);`
* `backgrond-color` 배경 | 색상 | `backgrond-color:#000;`
* `width` 가로넓이 혹은 가로크기 | `width:100px;`
* `height` 세로크기 | `height:200px;`
* `margin` 바깥여백 | `margin-top:50px;`
* `border-radius` 모서리 혹은 테두리 | 둥글게 | `border-radius:10px;`
* `font-weight` 글자 | 굵기 | 400 | `font-weight:800;`
* `font-family` 글자 | 꼴 | `font-family:'대표글꼴', '보조글꼴', sans-serif;`
## 위치속성 float
* 블록, 인라인 요소를 좌(left), 우(right) 사용하는 위치 속성
* 좌/우 배치하고 싶은 요소가 형제인 경우 사용
* 형제가 3개 이상인 경우 1->2 옆으로 두고 3을 내리고 싶은 경우, 형제3에게 `clear:both`를 선언하여 이전형제의 float 정렬 제거하기
## 오른쪽으로 보내고 싶은 형제 요소가 2개 이상이라면?
* 2개를 묶어서 그룹으로 처리하고 `float:right` 한번만 작성한다.
* `float:right`는 2번 이상 사용하면 역순이 되므로 **한번만 작성해야 한다!!**
### float를 적용하는 형제의 부모의 높이가 max-content(기본값)이라면?
* 부모의 높이를 제대로 인식못하므로 높이를 강제(px)시키거나 `overflow:hidden` 높이를 안주고 영역 재인식을 시켜 float에 의한 오류를 제거해야 한다.