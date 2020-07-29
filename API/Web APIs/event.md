Web API > Event
-

[Capturing and Bubbling phases]
- event.stopPropagation() : 이벤트 캡처링과 버블링에 있어 현재 이벤트 이후의 전파를 막는다.
- event.stopImmediatePropagation() : 같은 이벤트에서 다른 리스너들이 불려지는 것을 막는다.

❗ 위 두가지 메소드는 사용을 지양한다.

대신 부모에서

if (event.target !== event.currentTarget) { return; }

을 사용해서 사용한다.
