Operator
-

<h4> == : 추상 동등 연산자</h4>
- 타입 변환이 필요한 경우 타입 변환을 한 후에 동등한지 비교.

<br />

<h4> === : 완전 동등 연산자</h4> 
- 타입 변환을 하지 않으므로 두 값이 같은 타입이 아닌 경우 ===는 false를 반환.

---

<h3>Conditional (ternary) operator : 조건부 (삼항) 연산자</h3>
- 조건부 삼항 연산자는 자바스크립트에서 세 개의 피연산자를 취할 수 있는 유일한 연산자이다.
- 보통 `if` 명령문의 단축 형태로 쓰인다.

<br />

<h4> 조건 ? 참일 때 : 거짓일 때</h4>

문제 : 시간을 `23:7:15`가 아닌 `23:07:15`처럼 출력되게 만들어라.<br />
답안 : 삼항 연산자를 사용해서 시간/분/초의 숫자가 '0 < 10'일 때, 출력값 앞에 0이 생길 수 있게 만든다.
```
function getTime() {
    const date = new Date();
    const hours = date.getHours();
    const minutes = date.getMinutes();
    const seconds = date.getSeconds();
    element.innerText = `${hours < 10 ? `0${hours}` : hours}:${
        minutes < 10 ? `0${minutes}` : minutes
        }:${seconds < 10 ? `0${seconds}` : seconds}`; 
    }
}

function init() {
    getTime();
    setInterval(getTime, 1000);
}

init();
```
결과 : 23:21:29
