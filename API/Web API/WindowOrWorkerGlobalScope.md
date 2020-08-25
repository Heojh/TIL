Web API > WindowOrWorkerGlobalScope
-

<br>

<h4>Scheduling a call : 호출 스케줄링</h4>
'Scheduling a call'이란, 지금 당장 실행이 아닌 일정 시간이 지난 후에 원하는 함수를 예약 실행(호출)할 수 있게 하는 것을 말한다.<br>
- 호출 스케줄링을 구현하는 방법은 두 가지가 있다.<br>
    👉 `setTimeout` : 일정 시간이 지난 후에 함수를 실행<br>
    👉 `setInterval` : 일정한 시간 간격을 두고 함수를 실행

<br>

<h4>.setTimeout()</h4>
`setTimeout()` 메소드는 타이머가 만료되면 함수 또는 지정된 코드를 실행하는 타이머를 설정한다.<br>
```
// 3초 후에 경고창 호출.
const timeOut = setTimeout(() => alert('Game over!'), 3000);

// 매개변수 사용. 1초 후 announceScore() 호출.
function announceScore(user, score) {
    alert(`${user}님 ${score}점 입니다.`);
}

setTimeout(announceScore, 1000, 'Anna', 777); // Anna님 777점 입니다.
```
`clearTimeout()` 메소드는 `setTimeout`을 선택적으로 취소한다.
```
const timeOut = setTimeout(() => alert('Game over!'), 3000);

function timerStop() {
    clearTimeout(timeout);
}

stopBtn.addEventListener('click', timerStop);
```

<br>

<h4>.setInterval()</h4>
setInterval() 메소드는 각 호출 사이에 고정된 시간 지연으로 함수를 반복적으로 호출한다.<br>
```
// 1초 간격으로 1씩 감소.
const timer = setInterval(() => {
    let time = 10;
    if(time === 0) {
        clearInterval(timer); // 정지.
    } else {
        time--;
    }
}, 1000);
```
▶`clearInterval()` : 함수 호출 중단.