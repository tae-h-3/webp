# 📑 HTML 태그 정리

## 1. 문서 기본 태그
HTML 문서의 구조와 기본적인 레이아웃을 정의하는 태그들입니다.  

- `<html>` : HTML 문서의 시작과 끝을 나타냄  
- `<head>` : 문서의 메타데이터(제목, 스타일, 스크립트 등)를 포함  
- `<title>` : 브라우저 탭에 표시되는 문서 제목  
- `<body>` : 실제 화면에 표시되는 콘텐츠  
- `<h1>~<h6>` : 제목(heading), 숫자가 작을수록 더 큰 제목  
- `<p>` : 문단을 표시  
- `<hr>` : 구분선(horizontal rule)  
- `<br>` : 줄바꿈(line break)  

예시:  
```html
<html>
  <head>
    <title>HTML 기본</title>
  </head>
  <body>
    <h1>안녕하세요</h1>
    <p>이것은 문단입니다.</p>
    <hr>
    줄바꿈<br>다음 줄
  </body>
</html>
```

---

## 2. 텍스트 꾸미기 태그
문자에 강조, 취소선, 첨자 등을 적용해 글자 스타일을 바꿀 때 사용합니다.  

- `<b>` : 굵게(단순히 시각적 효과)  
- `<strong>` : 굵게 + 의미 강조  
- `<em>` : 기울임 + 의미 강조  
- `<i>` : 기울임(시각적 효과)  
- `<small>` : 작은 글씨  
- `<del>` : 취소선  
- `<ins>` : 밑줄(추가된 내용)  
- `<sup>` : 위 첨자  
- `<sub>` : 아래 첨자  
- `<mark>` : 형광펜 효과  

예시:  
```html
<p><b>굵게</b>, <strong>중요 강조</strong></p>
<p><em>기울임</em>, <i>단순 기울임</i></p>
<p><del>삭제된 글자</del>, <ins>추가된 글자</ins></p>
<p>H<sub>2</sub>O, E=mc<sup>2</sup></p>
<p><mark>중요한 부분</mark></p>
```

---

## 3. 블록 & 링크 태그
콘텐츠를 구획 나누거나 다른 페이지/위치로 이동하는 데 사용합니다.  

- `<pre>` : 입력한 그대로 표시 (공백/줄바꿈 유지)  
- `<div>` : 블록 단위 영역  
- `<span>` : 인라인 단위 영역  
- `<a>` : 하이퍼링크 (다른 페이지나 문서로 이동)  
- `<iframe>` : 웹페이지 안에 또 다른 페이지 삽입  

예시:  
```html
<pre>
    공백과 줄바꿈이
    그대로 유지됩니다.
</pre>

<div style="color:red;">블록 영역</div>
<span style="color:blue;">인라인 영역</span>

<a href="https://www.google.com">구글로 이동</a>

<iframe src="https://example.com" width="300" height="200"></iframe>
```

---

## 4. 메타 태그
문서의 정보나 외부 자원 연결을 위한 태그들입니다.  

- `<base>` : 문서의 기본 URL 지정  
- `<link>` : 외부 CSS 연결  
- `<script>` : 자바스크립트 코드 삽입  
- `<style>` : CSS 직접 작성  
- `<meta>` : 인코딩, 뷰포트 등 메타데이터 설정  
- `<title>` : 문서 제목(브라우저 탭 표시)  

예시:  
```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>메타 태그 예시</title>
  <link rel="stylesheet" href="style.css">
  <style>
    body { background-color: linen; }
  </style>
  <script>
    console.log("Hello, world!");
  </script>
</head>
```

---

## 5. 이미지 & 리스트 태그
이미지를 삽입하거나 항목을 나열할 때 사용합니다.  

- `<img>` : 이미지 삽입  
- `<ol>` : 순서 있는 목록 (ordered list)  
- `<ul>` : 순서 없는 목록 (unordered list)  
- `<dl>` : 설명 목록 (description list)  
- `<li>` : 리스트 항목 (list item)  
- `<dt>` : 용어(term)  
- `<dd>` : 설명(description)  

예시:  
```html
<img src="cat.jpg" alt="고양이" width="200">

<ol>
  <li>첫 번째</li>
  <li>두 번째</li>
</ol>

<ul>
  <li>사과</li>
  <li>바나나</li>
</ul>

<dl>
  <dt>HTML</dt>
  <dd>웹 문서 구조를 만드는 언어</dd>
</dl>
```

---

## 6. 표(table) 태그
데이터를 행과 열로 정리할 때 사용합니다.  

- `<table>` : 표 시작  
- `<caption>` : 표 제목  
- `<thead>` : 표의 머리글 영역  
- `<tbody>` : 본문 영역  
- `<tfoot>` : 요약 영역  
- `<tr>` : 행(row)  
- `<th>` : 제목 셀(굵게 + 중앙 정렬)  
- `<td>` : 일반 셀  

예시:  
```html
<table border="1">
  <caption>학생 성적표</caption>
  <thead>
    <tr><th>이름</th><th>점수</th></tr>
  </thead>
  <tbody>
    <tr><td>홍길동</td><td>90</td></tr>
    <tr><td>김철수</td><td>85</td></tr>
  </tbody>
  <tfoot>
    <tr><td>평균</td><td>87.5</td></tr>
  </tfoot>
</table>
```

---

## 7. 미디어 태그
오디오, 비디오, 외부 파일 등을 삽입합니다.  

- `<audio>` : 오디오 파일 삽입  
- `<video>` : 비디오 파일 삽입  
- `<embed>` : 외부 콘텐츠 삽입  
- `<object>` : 다양한 멀티미디어 객체 삽입  

예시:  
```html
<audio controls>
  <source src="music.mp3" type="audio/mpeg">
  브라우저가 오디오를 지원하지 않습니다.
</audio>

<video controls width="300">
  <source src="movie.mp4" type="video/mp4">
  브라우저가 비디오를 지원하지 않습니다.
</video>

<embed src="example.pdf" width="400" height="300">

<object data="game.swf" width="400" height="300"></object>
```

