## 4장. CSS3로 웹페이지 꾸미기

### 1. CSS3 스타일시트 개요
- **CSS (Cascading Style Sheets)**: HTML 문서의 스타일(색상, 폰트, 배치 등)을 정의하는 언어  
- **CSS3**: 최신 버전으로, 시각적 효과와 애니메이션, 반응형 웹 디자인 등을 지원  
- HTML은 구조, CSS는 표현을 담당 → 웹 개발의 역할 분리  
- 스타일시트를 적용하는 방법
  - 인라인 스타일 (`<p style="color:red;">`)
  - 내부 스타일 (`<style> ... </style>`)
  - 외부 스타일 (`<link rel="stylesheet" href="style.css">`)

### 2. CSS3 스타일시트 만들기
- 외부 CSS 파일 생성: `style.css`
- HTML 문서에서 `<head>` 안에 `<link>` 태그로 불러오기
- 장점: 재사용성 ↑, 유지보수 용이, 코드 간결화

### 3. 셀렉터
- HTML 요소를 선택하여 스타일을 적용하는 방법
- 주요 셀렉터 종류
  - 태그 선택자: `p { color: blue; }`
  - 클래스 선택자: `.highlight { background: yellow; }`
  - 아이디 선택자: `#header { font-size: 20px; }`
  - 그룹 선택자: `h1, h2, h3 { color: gray; }`
  - 자손/자식 선택자: `div p {}`, `div > p {}`
  - 가상 클래스: `a:hover { color: red; }`, `nth-child()` 등

### 4. 색과 텍스트 꾸미기
- 색 표현 방식
  - 이름: `red`, `blue`
  - RGB: `rgb(255, 0, 0)`
  - HEX: `#ff0000`
  - RGBA (투명도 포함): `rgba(0,0,0,0.5)`
- 텍스트 꾸미기 속성
  - 글꼴: `font-family: Arial;`
  - 크기: `font-size: 16px;`
  - 두께: `font-weight: bold;`
  - 기울임: `font-style: italic;`
  - 정렬: `text-align: center;`
  - 장식: `text-decoration: underline;`
  - 그림자: `text-shadow: 2px 2px 5px gray;`

### 5. 박스 모델
- HTML 요소는 모두 박스 형태로 표현됨
- 구성 요소: **content → padding → border → margin**
- 속성 예시
  - `width`, `height`
  - `margin: 10px;`
  - `padding: 5px;`
  - `border: 1px solid black;`
- `box-sizing: border-box;` → padding과 border를 포함한 크기 계산

### 6. 시각적 효과
- 그림자 효과: `box-shadow`
- 둥근 모서리: `border-radius`
- 배경 관련 속성: `background-image`, `background-size`, `background-repeat`
- 투명도: `opacity`
- 그라데이션: `linear-gradient`, `radial-gradient`
- 트랜지션(transition): 부드러운 변화 효과

---

## 5장. CSS3 고급 활용

### 1. 배치
- **position** 속성: `static`, `relative`, `absolute`, `fixed`, `sticky`
- **float**: 이미지나 박스를 좌우로 띄움
- **flexbox**: 1차원 레이아웃 정렬 방식
- **grid**: 2차원 레이아웃 설계 가능
- `z-index`: 요소의 쌓임 순서 제어

### 2. 리스트 꾸미기
- 불릿 모양 변경: `list-style-type: square;`
- 이미지로 불릿 대체: `list-style-image: url("star.png");`
- 위치 조정: `list-style-position: inside;`
- 수평 메뉴 만들기 → `display: inline;`

### 3. 표 꾸미기
- 테두리: `border-collapse: collapse;`
- 행/열 색상: `nth-child()` 활용
- 셀 여백: `padding`
- 표의 스타일링: `caption-side`, `border-spacing`

### 4. 폼 꾸미기
- 입력창 스타일: `input[type="text"] { border: 1px solid gray; }`
- 버튼 스타일: `button { background: blue; color: white; }`
- 포커스 효과: `input:focus { outline: 2px solid skyblue; }`
- placeholder 스타일링: `::placeholder`

### 5. CSS3 스타일로 태그에 동적 변화 만들기
- **가상 클래스(pseudo-class)** 활용
  - `:hover`, `:active`, `:focus`, `:nth-child()` 등
- **가상 요소(pseudo-element)** 활용
  - `::before`, `::after`
- 애니메이션
  - `@keyframes` 정의 후 `animation` 속성 사용
  - 예: `animation: slidein 2s infinite;`
- 트랜스폼(transform)
  - `rotate`, `scale`, `translate`, `skew`
- 트랜지션(transition)
  - `transition: all 0.3s ease-in-out;`