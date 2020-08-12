String
-
- path : JavaScript reference > Standard built-in objects > String

<br>

<h4>String.prototype.charAt()</h4>
- charAt() 메소드는 문자열에서 특정 인덱스에 위치하는 유니코드 단일 문자를 반환한다.<br>

<h4>**Project : 끝말잇기**</h4>
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
