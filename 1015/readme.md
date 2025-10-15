# 7장. 자바스크립트 코어 객체와 배열

## 1. 객체 개념

### 자바스크립트 객체
- 자바스크립트에서 객체는 프로퍼티(속성)와 메소드(함수)로 구성된 데이터의 집합이다.
- 객체는 현실 세계의 사물을 표현하거나, 데이터와 동작을 하나의 단위로 묶는 데 사용된다.

### 자바스크립트 객체의 유형
- **내장 객체 (Core Object)** : Array, String, Date, Math 등 자바스크립트에서 기본적으로 제공하는 객체.
- **브라우저 객체 (BOM)** : window, navigator, screen 등 브라우저 환경에서 제공되는 객체.
- **문서 객체 (DOM)** : HTML 문서를 객체로 표현한 것으로, document 객체를 통해 접근할 수 있다.
- **사용자 정의 객체** : 프로그래머가 직접 생성하는 객체.

---

## 2. 코어 객체 다루기

### 코어 객체 종류
- 대표적인 코어 객체:
  - **Object**
  - **Array**
  - **Date**
  - **String**
  - **Math**

### new 키워드로 코어 객체 생성
```javascript
let obj = new Object();
let arr = new Array();
let str = new String("Hello");
let date = new Date();
```

### 객체 접근 
- **점 표기법** : `object.property`
- **대괄호 표기법** : `object["property"]`
```javascript
let person = { name: "홍길동", age: 25 };
console.log(person.name);        // 홍길동
console.log(person["age"]);      // 25
```

---

## 3. 배열과 Array

### 배열을 만드는 방법 
1. 대괄호 `[]` 사용  
2. `new Array()` 사용

### []로 배열 만들기 

#### 배열 만들기
```javascript
let fruits = ["apple", "banana", "cherry"];
```

#### 배열 크기와 원소 추가 
```javascript
let arr = [];
arr[0] = "a";
arr[1] = "b";
arr.push("c");  // push 메소드로 추가
```

### Array로 배열 만들기 

#### 초기 값을 가진 배열 생성
```javascript
let nums = new Array(1, 2, 3, 4);
```

#### 초기화되지 않은 배열 생성
```javascript
let emptySlots = new Array(5);  // 길이 5, 비어있는 배열
```

#### 빈 배열 생성
```javascript
let empty = new Array();
```

### 배열의 원소 개수, length 프로퍼티
```javascript
let arr = [10, 20, 30];
console.log(arr.length); // 3
```

### 배열의 특징 

#### 배열은 Array 객체이다
- 자바스크립트에서 배열은 특수한 객체 형태이다.
- 배열의 인덱스는 문자열로 저장되며, length 프로퍼티를 통해 길이를 관리한다.

#### 배열에는 여러 타입의 데이터가 섞여 저장될 수 있다
```javascript
let mixed = [1, "hello", true, {a:1}, [1,2]];
```

### Array 객체의 메소드 활용 
- `push()`, `pop()`, `shift()`, `unshift()`
- `splice()`, `slice()`
- `indexOf()`, `forEach()`, `map()`, `filter()`, `reduce()`

---

## 4. Date
- 날짜와 시간을 다루는 객체
```javascript
let now = new Date();
console.log(now.toLocaleString());
```

---

## 5. String 

### String 객체
- 문자열을 다루는 객체

### String 객체는 수정 불가
- 문자열은 immutable (불변)이다. 수정 시 새로운 문자열이 생성된다.

### 문자열 길이, length
```javascript
let str = "Hello";
console.log(str.length); // 5
```

### []로 문자 접근
```javascript
console.log(str[1]); // 'e'
```

### String 메소드
- `charAt()`, `indexOf()`, `substring()`, `toUpperCase()`, `toLowerCase()`, `split()`, `trim()` 등

### String 활용

#### 문자열 비교
```javascript
"abc" === "abc"  // true
```

#### 문자열 연결
```javascript
"Hello" + " " + "World";
```

#### 서브 스트링 찾기
```javascript
let text = "JavaScript";
console.log(text.indexOf("Script")); // 4
```

#### 서브스트링 리턴
```javascript
console.log(text.substring(0, 4)); // Java
```

#### 문자열 변경
```javascript
let msg = "Hi";
msg = msg.replace("Hi", "Hello");
```

#### 대소문자 변경
```javascript
"hello".toUpperCase();
"HELLO".toLowerCase();
```

#### 문자열 분할
```javascript
"apple,banana,cherry".split(",");
```

#### 문자열 앞뒤의 공백 제거 
```javascript
"   hello   ".trim();
```

#### 문자열 내의 문자 알아내기 
```javascript
let s = "ABC";
console.log(s.charAt(1)); // B
```

---

## 6. Math

### 난수 발생
```javascript
console.log(Math.random()); // 0 이상 1 미만 난수
```

---

## 7. 사용자 객체 만들기 

### new Object()로 객체 만들기

#### 사용자 객체 만들기
```javascript
let user = new Object();
user.name = "홍길동";
user.age = 25;
```

#### 사용자 객체의 프로퍼티 사용
```javascript
console.log(user.name);
```

#### 사용자 객체에 메소드 만들기
```javascript
user.sayHello = function() {
  console.log("안녕하세요!");
};
user.sayHello();
```

### 리터럴 표기법으로 객체 만들기
```javascript
let person = {
  name: "이몽룡",
  age: 20,
  hello: function() {
    console.log("안녕!");
  }
};
```

### 프로토타입의 개념과 사용자 객체 만들기

#### 프로토타입은 함수로 만든다
```javascript
function Student(name, age) {
  this.name = name;
  this.age = age;
}
```

#### new로 객체를 생성하고 활용한다
```javascript
let s1 = new Student("홍길동", 21);
console.log(s1.name);
```
