Array
-

List
- Array.of()
- Array.from()
- .forEach()
- .map()
- .forEach() 와.map() 차이
- .join()

<br />

<h4>Array.of()</h4>
- Array.of() 메서드는 인자의 수나 유형에 관계없이 가변 인자를 갖는 새 Array 인스턴스를 만든다.
- Array.of()와 Array 생성자의 차이는 정수형 인자의 처리 방법에 있다. Array.of(7)은 하나의 요소 7을 가지 배열을 생성하지만 Array(7)은 length 속성이 7인 빈 배열을 생성한다.

<br />

<h4>Array.from()</h4>
- Array.from() 메서드는 유사 배열 객체(array-like object)나반복 가능한 객체(iterable object)를 얕게 복사해서 새로운Array 객체를 만듭니다.
- Array.from()은 선택 매개변수인 mapFn(맵핑함수)를 가지는데,배열(혹은 배열 서브클래스)의 각 요소를맵핑할 때 사용할 수 있습니다.

```
const buttons = document.querySelectorAll('.btn');
Array.from(buttons).forEach(button => {
    button.addEventListener('click', () => console.log('hola'));
});
```

<br />

<h4>Array.prototype.forEach()</h4>
- 배열의 요소를 반복한다.
- 각 요소에 대한 콜백을 실행한다.
- 값을 반환하지 않는다.

```
const buttons = document.querySelectorAll('.btn');
Array.from(buttons).forEach(button => {
    button.addEventListener('click', () => console.log('hola'));
});
```

<br />

<h4>Array.prototype.map()</h4>
- 배열의 요소를 반복한다.
- 각 요소에서 함수를 호출하여 결과로 새 배열을 작성하여 각 요소를 새 요소에 매핑한다.

<br />

<h4>.forEach() 와 .map()의 차이</h4>
- .map()은 새로운 배열을 반환한다.
- 원본 배열을 견경하고 싶지 않으면, .map()을 사용한다.
- 단순히 배열을 반복할 필요가 있다면 .forEach()를 사용한다.

<br />

<h4>Array.prototype.join()</h4>
- .join() 메소드는 배열의 모든 요소를 연결해 하나의 문자열로 만든다. <br />
- arr.join(각 요소를 구분할 문자열) 