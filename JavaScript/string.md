String
-
path : JavaScript reference > Standard built-in objects > String <br />

List
- .charAt()
- .replace()
- .split()
- .substring()
- .concat()
- .includes()
- .repeat()

<br>

<h3>String.prototype.charAt()</h3>
- charAt() 메소드는 문자열에서 특정 인덱스에 위치하는 유니코드 단일 문자를 반환한다.<br>

<h4>Project : 끝말잇기</h4>

```
const question = '나무';
const answer = '무리수;

// question 마지막 문자 반환.
const questionLastChar = question.charAt(question.length-1);

// answer 첫 번째 문자 반환.
const answerFirstChar = answer.charAt(0);

console.log(questionLastChar); // '무'
console.log(answerFirstChar); // '무'
```
▶ question.charAt(1) 을 해도 되지만,<br>
단어를 이루는 문자의 갯수가 달라질 수 있기 때문에 question.chatAt(**question.length-1**)을 사용한다.

<br>

<h3>String.prototype.replace()</h3>
- replace() 메소드는 주어진 패턴에 일치하는 일부 또는 모든 부분이 교체된 새로운 문자열을 반환.<br>

<h4>Project : 끝말잇기(점수판)</h4>

```
let score = '점수 : 100';

function paintScore(num) {
    const getScore = Number(score.replace(/[^0-9]/g,'')) + num;
    console.log(getScore); // 200
    console.log(typeof getScore); // number
    score = getScore >= 0 ? `점수 : ${getScore}` : `점수 : 0`;
    console.log(typeof score); // string
}

paintScore(100); // '점수 : 200'
paintScore(-50); // '점수 : 50'
```
▶ 숫자만 반환하는 정규표현식 : (/[^0-9]/g,'')<br>
▶ 문자를 숫자로 형변환 : Number()

<br />

<h3>String.prototype.split()</h3>
.split() 메소드는 String 객체를 지정한 구분자를 이용하여 여러개의 문자열로 나눈다. <br />

<h4>Project : Bulls and Cows</h4>
사용자가 누른 네자리 수(문자열)를 배열로 만들기 <br />

```
const inputNumber = "2514";
const strArray = inputNumber.split('');
console.log(strArray) // ["2", "5", "1", "4"]
```
or

```
const strArray = [...'sky is blue'];        
console.log(strArray); // ["s", "k", "y", " ", "i", "s", " ", "b", "l", "u", "e"]
```

<br />

<h3>String.prototype.substring()</h3>
.substring() 메소드는 string 객체의 시작 인덱스로부터 종료 인덱스 전 까지 문자열의 부분 문자열을 반환한다. <br />

```
// 입력한 번호 끝에서부터 지우기.
const deleteBtn = document.querySelector('.delete');
deleteBtn.addEventListener('click', () => {
	let numberChange = paintNumber.textContent;
	numberChange = numberChange.substring(0, numberChange.length - 1);
	paintNumber.textContent = numberChange;
}
```

<br />

<h3>String.prototype.concat()</h3>
.concat() 메소드는 매개변수로 전달된 모든 문자열을 호출 문자열에 붙인 새로운 문자열을 반환한다. <br />

```
const strFirst = 'Hello';
const strSecond = 'World';

console.log(strFirst.concat(' ', strSecond); // Hello World
console.log(strSecond.concat(', ', strFirst); // World, Hello
```

<br />

<h3>String.prototype.includes()</h3>
.includes() 메서드는 배열이 특정 요소를 포함하고 있는지 판별한다.

```
const isEmail = email => email.includes('@');
consoel.log(isEmail('heojh@github.com')); // true
```

<br />

<h3>String.prototype.repeat()</h3>
.repeat() 메서드는 문자열을 주어진 횟수만큼 반복해 붙인 새로운 문자열을 반환한다.

```
const CC_NUMBER = '6060';
const displayName = `${'****-'.repeat(3)}${CC_NUMBER}`;
console.log(displayName); // ****-****-****-6060
```
