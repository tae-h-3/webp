# 8장. HTML DOM과 Document

## 1. HTML DOM 개요  
- DOM(Document Object Model)이란?  
  - 웹 브라우저가 HTML 문서를 읽을 때, 태그 하나하나를 객체(Object)로 생성하고 이 객체들이 트리(Tree) 구조로 연결된 형태.  
  - 루트(root) 객체는 document 객체이며, 실제 HTML 문서 요소들이 그 하위에 자식(child) 객체로 존재.  
- 왜 중요한가?  
  - DOM을 통해 스크립트(JavaScript)로 HTML 요소의 속성, 스타일, 콘텐츠 등을 동적으로 제어할 수 있다.  
- DOM의 구성과 특징  
  - 객체 노드: 요소(Element), 속성(Attribute), 텍스트(Text) 등  
  - 부모-자식 관계(parent-child), 형제(sibling) 관계 등이 트리 구조로 표현됨.  
  - 브라우저 로딩 시점(load) 이후 DOM 트리가 완성됨 → 그 이후에 스크립트로 상호작용 가능.  

## 2. DOM 객체 다루기  
- 요소 선택 및 참조  
  - `getElementById(id)`, `getElementsByTagName(tag)`, `getElementsByClassName(class)` 등의 메소드 사용.  
  - 예: `document.getElementsByTagName("span")` → 모든 `<span>` 요소를 배열 형태로 반환.  
- 프로퍼티(property) 및 메소드(method) 활용  
  - `innerHTML`, `textContent`, `style`, `setAttribute()`, `removeAttribute()` 등  
  - 예: `요소.style.backgroundColor = "yellow"; 요소.setAttribute("id","myDIV");`  
- DOM 객체의 탐색 및 수정  
  - 부모(`parentNode`), 자식(`childNodes`/`children`), 형제(`nextSibling`/`previousSibling`) 등을 통해 트리를 탐색 가능  
  - 동적 생성: `document.createElement()`, `appendChild()` 등을 이용하여 문서에 새로운 요소 삽입.  
- 실습 예제 및 주의사항  
  - 태그 이름 대소문자 주의  
  - `getElementsByTagName()` 뒤에 복수형 ‘s’ 필요.  
  - 스타일 적용 시 정확한 프로퍼티명 사용: ex) `backgroundColor`, `fontSize` 등.  

## 3. document 객체  
- document 객체의 주요 역할  
  - HTML 문서 전체를 표현하는 객체로, DOM 트리의 진입점(entry point) 역할  
  - URL, 도메인, title, lastModified, activeElement 등 다양한 프로퍼티 제공.  
- 주요 프로퍼티 및 메소드  
  - `document.URL`, `document.location`, `document.title`, `document.domain`, `document.readyState` 등.  
  - `document.getElementById()`, `document.getElementsByTagName()`, `document.write()` 등.  
  - `document.documentElement` → HTML 문서 최상위 `<html>` 요소.  
- 문서 로딩 상태와 readyState  
  - `document.readyState`는 문서의 로딩 상태(loading, interactive, complete 등)를 나타냄.  
- 주의 사항  
  - `document.write()` 사용 시 페이지 로딩 이후에 호출하면 기존 내용이 지워질 수 있으므로 주의  
  - 직접 조작한 요소나 스타일이 많아지면 코드 유지보수가 어려워질 수 있음 → 구조화된 접근 필요  

## 4. HTML 문서의 동적 구성  
- 동적 구성의 개념  
  - 웹 페이지가 처음 로드된 이후 JavaScript를 통해 새로운 요소를 생성하거나 기존 요소를 제거·변경하여 동적으로 구성하는 방식  
- 생성(Create), 삽입(Insert), 삭제(Delete)  
  - `createElement()`, `createTextNode()`, `appendChild()`, `insertBefore()`, `removeChild()` 등이 사용됨.  
  - 예:  
    ```js
    var newDIV = document.createElement("div");
    newDIV.innerHTML = "새로 생성된 DIV입니다.";
    newDIV.setAttribute("id", "myDIV");
    newDIV.style.backgroundColor = "yellow";
    document.getElementById("parent").appendChild(newDIV);
    ```  
- 문서 구조 변경 시 유의사항  
  - 메모리 누수(memory leak)나 불필요한 DOM 노드 증가로 인한 성능 저하 주의  
  - 변화를 최소화할 수 있는 설계(예: 이벤트 위임) 고려  
- 활용 사례  
  - 사용자 입력에 따라 폼 요소 추가  
  - AJAX 통신으로 받은 데이터를 기반으로 DOM 생성  
  - 애니메이션이나 인터랙티브 UI 구성 등  
- 요약 및 장점  
  - DOM 조작을 통해 정적 페이지가 아닌 **인터랙티브하고 반응적인 웹 애플리케이션** 구현 가능  
  - 구조화된 코딩과 적절한 DOM 접근 방식이 유지보수성과 성능에 크게 기여  

---

**요약 한 문장**  
> 8장에서는 브라우저 내부에서 HTML 문서를 객체 트리로 표현한 DOM 구조를 이해하고, document 객체를 통해 요소를 선택·조작하며, 나아가 자바스크립트로 문서를 동적으로 구성하는 방법을 학습한다.
