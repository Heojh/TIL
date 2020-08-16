Math
-
- path : JavaScript reference > Standard built-in objects > Math

<br />

<h4>Math.random()</h4>
- Math.random() 메소드는 0이상 1미만의 구간에서 근사적으로 균일한 부동소숫점 의사난수를 반환하며,<br/ >
이 값은 사용자가 원하는 범위로 변형할 수 있다.<br />

<h4>Project : 끝말잇기</h4>
1에서 9까지의 숫자 중 임의의 숫자 만들기.

```
function Random(min, max) { // --- 1
	min = Math.ceil(min);  // --- 2
	max = Math.floor(max); // --- 3
	this.num = Math.floor(Math.random() * (max - min + 1)) + min;
}
let firstNum = new Random(1,9);
let secondNum = new Random(1,9);
console.log(firstNum.num);
console.log(secondNum.num);
```

▶ 1. 생성자 함수 Random() <br />
▶ 2. `Math.ceil()` : 전달된 실수의 소수 부분을 무조건 올림. <br />
▶ 3. `Math.floor()` : 전달된 실수의 소수 부분을 무조건 내림. <br />

<h4>Project : 숫자야구</h4>
1에서 9까지의 숫자 중 중복이 없는 임의의 수 3개 배열에 담기.

```
function selectNum() {
	let numbers=[];
	let amonut = 3;
	for(let insertCur = 0; insertCur < amonut; insertCur++) { // --- 1
		numbers[insertCur] = Math.floor(Math.random() * 9) + 1;
		for(let searchCur = 0; searchCur < insertCur; searchCur++) { // ---2
			if(numbers[insertCur] === numbers[searchCur]) {
				insertCur--;
				break;
			}
		}
	}
	console.log(numbers); // [num1, num2, num3]
    const changeStr = numbers.join(''); // --- 3
    console.log(changeStr); // 'num1num2num3'
}

selectNum();
```

▶ 1. 임의의 수 삽입  <br />
▶ 2. 중복 검사  <br />
▶ 3. `array.join()` : 배열의 모든 요소를 연결해 하나의 문자열로 만든다.  <br />