# HTML5의 문서 구조화와 웹 폼

## 1. HTML5의 문서 구조와 시맨틱 태그

HTML5에서는 웹 문서를 의미 있게 나누기 위해 시맨틱 태그를 도입하였다.
시맨틱 태그를 사용하면 문서 구조가 명확해지고, 검색 엔진 최적화(SEO)와
접근성 향상에 도움을 준다.

-   `<header>` : 문서나 섹션의 머리말 영역, 보통 로고, 제목, 메뉴 등이
    위치\
-   `<nav>` : 내비게이션 메뉴, 다른 페이지나 같은 문서 내의 주요 링크
    모음\
-   `<section>` : 주제별로 나누는 구역, 기사, 소개글 등 독립적인 단위\
-   `<article>` : 독립적으로 배포하거나 재사용 가능한 콘텐츠
    블록(게시글, 뉴스 기사 등)\
-   `<aside>` : 본문 내용과 간접적으로 관련된 보조 콘텐츠(광고, 사이드바
    등)\
-   `<footer>` : 문서나 섹션의 꼬리말, 저작권 정보, 연락처, 링크 등

------------------------------------------------------------------------

## 2. 시맨틱 블록 태그

콘텐츠를 더 풍부하게 표현할 수 있는 블록 태그들이 있다.

-   `<figure>` : 이미지, 다이어그램, 코드 블록 등 독립적인 콘텐츠 단위\
-   `<figcaption>` : `<figure>` 안의 설명 캡션\
-   `<details>` : 사용자가 클릭하여 펼치거나 접을 수 있는 콘텐츠 영역\
-   `<summary>` : `<details>`의 제목 부분

예시:

``` html
<figure>
  <img src="diagram.png" alt="웹 구조 다이어그램">
  <figcaption>HTML5 문서 구조 예시</figcaption>
</figure>

<details>
  <summary>더 알아보기</summary>
  <p>HTML5에서는 시맨틱 태그 덕분에 문서 구조가 명확해집니다.</p>
</details>
```

------------------------------------------------------------------------

## 3. 웹 폼 태그

웹 폼은 사용자가 입력한 데이터를 서버로 전송하기 위해 사용한다.

-   `<form>` : 폼 전체를 감싸는 태그\
-   `action` : 데이터를 전송할 URL 지정\
-   `enctype` : 전송할 데이터의 인코딩 방식 (예:
    `application/x-www-form-urlencoded`, `multipart/form-data`)\
-   `method` : 데이터 전송 방식 (`GET` 또는 `POST`)\
-   `name` : 폼의 이름\
-   `target` : 데이터를 전송한 후 응답을 표시할 위치 지정 (`_blank`,
    `_self` 등)

------------------------------------------------------------------------

### 1. 텍스트 입력

``` html
<form>
  이름: <input type="text" name="username" placeholder="이름을 입력하세요">
</form>
```

### 2. 텍스트/이미지 버튼 만들기

``` html
<input type="submit" value="제출">
<input type="image" src="button.png" alt="이미지 버튼">
```

### 3. 체크박스/라디오버튼/콤보박스 만들기

``` html
취미:
<input type="checkbox" name="hobby" value="sports"> 스포츠
<input type="checkbox" name="hobby" value="music"> 음악

성별:
<input type="radio" name="gender" value="male"> 남성
<input type="radio" name="gender" value="female"> 여성

과목 선택:
<select name="subject">
  <option value="html">HTML</option>
  <option value="css">CSS</option>
  <option value="js">JavaScript</option>
</select>
```

### 4. `<label>`로 폼 요소의 캡션 만들기

``` html
<label for="email">이메일:</label>
<input type="email" id="email" name="email">
```

### 5. 색 입력

``` html
색상 선택: <input type="color" name="favcolor">
```

### 6. 시간 정보 입력

``` html
날짜: <input type="date" name="date">
시간: <input type="time" name="time">
```

### 7. 스핀버튼과 슬라이드바로 편리한 숫자 입력

``` html
나이: <input type="number" name="age" min="0" max="100">
볼륨: <input type="range" name="volume" min="0" max="100">
```

### 8. 입력할 정보의 힌트 보여주기

``` html
<input type="text" name="userid" placeholder="아이디를 입력하세요">
```

### 9. 형식을 가진 텍스트 입력

``` html
이메일: <input type="email" name="email">
웹사이트: <input type="url" name="homepage">
전화번호: <input type="tel" name="phone">
```

### 10. 폼 요소들의 그룹핑, `<fieldset>`

``` html
<fieldset>
  <legend>회원 정보</legend>
  이름: <input type="text" name="username"><br>
  이메일: <input type="email" name="email">
</fieldset>
```
