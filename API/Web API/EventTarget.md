Web API > EventTarget
-

<br />

<h4>EventTarget.addEventListener()</h4>
EventTarget에 특정 이벤트 유형의 이벤트 처리기를 등록한다.

<h4>{once: true}</h4>
이벤트를 한 번만 실행가능.

<h5>Project : Bulls and Cows</h5>

```
element.addEventListener('click', (e) => {
    console.log('Hello World');
}, {once: true});
```
❗ 클릭한 버튼을 다시 클릭하지 못하게 만들려고 하였으나 <br /> 
실수로 번호를 클릭하고 지우면 그 번호를 다시 누를 수 없는 문제가 발생.

<br />

<h4>EventTarget.removeEventListener()</h4>
EventTarget에서 주어진 이벤트 수신기를 제거한다.

<br />

<h4>EventTarget.dispatchEvent()</h4>
EventTarget에 이벤트를 디스패치한다.