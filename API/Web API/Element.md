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

[Scroll] <br />
element.scrollIntoView() : 선택된 요소를 브라우저 창의 보이는 영역으로 스크롤. <br />

element.scrollTop() : 요소안의 현재 스크롤바의 위치값을 반환.
```
// 현재 보고있는 브라우저의 높이
$(window).height(); 

// 현재 스크롤바의 위치 값.
// 스크롤을 맨 위로 올리려면 $(window).scrollTop(0)을 해주면 됨.
$(window).scrollTop();

// 현재 보고 있는 브라우저의 맨 밑 바닥의 높이
$(window).height + $(window).scrollTop();

//원하는 위치까지 천천히 올라가게 하려면?
$('html, body').animate({scrollTop: 가고싶은 위치}, 가는데 걸리는 시간);
// ※ 1000 = 1초

// document안의 상대적인 현재 위치값을 알 수 있음.
offset();

// 요소의 상단 부분에서의 거리 좌표
offset().top;

// 요소의 왼쪽에서 부터의 거리 좌표
offset().left;
```

<br />

<h3>.getBoundingClientRect()</h3>
element의 크기와 뷰포트를 기준으로 한 위치를 반환한다. <br />

```
const field = document.querySelector('.game__field');
const fieldRect = field.getBoundingClientRect();
// When the starting point is (0,0)
const xStart = 0;
const xEnd = fieldRect.width;
const yStart = 0;
const yEnd = fieldRect.height;
```

<br />

<h3>.matches()</h3>
.matched() 메서드는 제공된 selectorString에 의해 요소가 선택되는지 점검한다.
```
function onFieldClick(event) {
    if(!started) {
        return
    }
    const target = event.target;
    if(target.matches('.carrot')) {
        target.remove();
        score ++;
        playSound(carrotSound);
        updateScoreBoard();
        if (score === CARROT_COUNT) {
            finishGame(true);
        }
    } else if(target.matches('.bug')) {
        finishGame(false);
    }
}
```