Array
-

> Array.of()
- Array.of() 메서드는 인자의 수나 유형에 관계없이 가변 인자를 갖는 새 Array 인스턴스를 만든다.
- Array.of()와 Array 생성자의 차이는 정수형 인자의 처리 방법에 있다. Array.of(7)은 하나의 요소 7을 가지 배열을 생성하지만 Array(7)은 length 속성이 7인 빈 배열을 생성한다.


> Array.from()
- Array.from() 메서드는 유사 배열 객체(array-like object)나반복 가능한 객체(iterable object)를 얕게 복사해새로운Array 객체를 만듭니다.
- Array.from()은 선택 매개변수인 mapFn(맵핑함수)를 가지는데,배열(혹은 배열 서브클래스)의 각 요소를맵핑할 때 사용할 수 있습니다.
