Hoisting
-
: 인터프린터가 자바스크립트 코드를 해석함에 있어서 Global 영역의 선언된 코드블럭을 최상의 Scope로 끌어올리는 것을 호이스팅이라 한다.

####사전적 의미:
- 끌어올리다.

####무엇을 끌어올리는가?
- 변수 '선언'
- 함수 '선언'


> 코드를 실행하기 전 단계

```
console.log(a());
console.log(b());
console.log(c());

// 함수 선언문 : 함수 선언
function a() {
    return 'a';
}

// 함수 표현식 : 변수 선언 & 할당
var b = function banilla() {
    return 'b';
}
// 표현식으로 정의된 함수의 함수명(banilla)은 함수내부에서만 사용할 수 있고 함수 외부에서는 사용할 수 없다.
   

// 함수 표현식 : 변수 선언 & 할당
var c = function() {
    return 'c';
}
```

> 자바스크립트 엔진이 실제로 실행할 내용
```
// 함수 선언
function a() {
    return 'a';
}
var b; // 변수 선언
var c; // 변수 선언

console.log(a());
console.log(b());
console.log(c());

// 변수 할당
b = function funcB() {
    return 'b';
}

// 변수 할당
c = function() {
    return 'c';
}
```

> 출력 결과
```
a
Uncaught TypeError: b is not a funtion
Unvaught TypeError: c is not a funtion
```