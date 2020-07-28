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

// (기명)함수 표현식 : 변수 선언 & 할당
var b = function banilla() {
    return 'b';
}
// 표현식으로 정의된 함수의 함수명(banilla)은 함수내부에서만 사용할 수 있고 함수 외부에서는 사용할 수 없다.
   

// (익명)함수 표현식 : 변수 선언 & 할당
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
- 함수 선언문 : 함수 전체가 Hoisting의 대상.
- 함수 표현식 : 선언된 변수만 Hoisting.

####결론
안전하고 예측 가능한 소스를 위해서 함수 표현식을 쓸 것을 권한다.
- 함수 선언문 방식이 꼭 필요한 경우는 **즉시실행함수**나 **콜백함수에 대입하는 익명함수 선언** 뿐이다.<br/>
엄밀히 말하면 위의 두가지 경우 선언시 변수에 할당하는 과정이 없으므로 '호이스팅 등으로 인해 종종 문제를 일으키는' 함수 선언문의 범주에 속하지 않는다고 할 수 있다.<br />
그밖에 모든 함수를 함수 표현식만으로 구성해도 된다.