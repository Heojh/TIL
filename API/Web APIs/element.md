Web API > Element
-

[Coordinates]
- 브라우저의 좌측 상단 = (0,0)
- 우측 아래로 갈수록 x, y 값이 증가
- X축 : 수평축 / Y축 : 수직축

element.getBoundingClientRect() : 요소의 사이즈나 위치에 관련된 다양한 정보를 알 수 있다.
- top : 위에서부터 요소의 상단까지의 거리 = y값
- left : 왼쪽에서부터 요소의 좌측까지의 거리 = x값
- bottom : 위에서부터 요소의 하단까지의 거리 = y값
- right : 왼쪽에서부터 요소의 우측까지의 거리 = x값
- event.client : 브라우저에서 떨어진 x, y의 거리
- event.page : 페이지 자체에서 떨어진 x, y의 거리

[Scroll]
- element.scrollIntoView() : 선택된 요소를 브라우저 창의 보이는 영역으로 스크롤.