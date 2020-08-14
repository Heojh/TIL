Math
-
- path : JavaScript reference > Standard built-in objects > Math

<br />

<h4>Math.random()</h4>
- Math.random() 메소드는 0이상 1미만의 구간에서 근사적으로 균일한 부동소숫점 의사난수를 반환하며,<br/ >
이 값은 사용자가 원하는 범위로 변형할 수 있다.<br />

<h4>Project : 끝말잇기</h4>

```
function Random(min, max) { // ---1
	min = Math.ceil(min);  // ---2
	max = Math.floor(max); // ---3
	this.num = Math.floor(Math.random() * (max - min + 1)) + min;
}
let firstNum = new Random(1,9);
let secondNum = new Random(1,9);
console.log(firstNum.num);
console.log(secondNum.num);
```

▶ 1. 생성자 함수 Random() <br >
▶ 2. `Math.ceil()` : 전달된 실수의 소수 부분을 무조건 올림. <br />
▶ 3. `Math.floor()` : 전달된 실수의 소수 부분을 무조건 내림. <br />

