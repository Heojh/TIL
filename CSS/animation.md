Animation
-
- CSS는 JavaScript 또는 Flash를 사용하지 않고도 HTML 요소의 애니메이션을 허용한다. <br />
- `@keyframes`를 사용하여 애니메이션 효과를 줄 수 있다. <br />

<br />

<h4>from, to</h4>

```
// from, to를 사용하여 애니메이션 효과를 줌.
@keyframes example {
    from { // --- 1
        background-color: red;
    }
    to { // --- 2
        background-color: blue;
    }
}

body {
    background-color: red;
    animation: example 4s;
}
```
▶ 배경색이 red -> blue로  변경됨.(4초 소요) <br />
▶ 1. from : 0%, 시작 <br />
▶ 2. to : 100%, 완료 <br />

<br />

<h4>percentage : 백분율</h4>

```
// 백분율로 단계를 나눠서 애니메이션 효과를 줌.
@keyframes example {
  0%   {background-color: red;}
  25%  {background-color: yellow;}
  50%  {background-color: blue;}
  100% {background-color: green;}
}

body {
    background-color: red;
    animation: example 4s;
}
```
▶ 배경색이 red -> yellow -> blue -> green 순서로 변경됨. (4초 소요) <br />

<br />

<h4>애니메이션이 가능한 속성</h4>

애니메이션 이름 <br />
animation-name: none <br />

애니메이션이 완료하는데 소요되는 시간 <br/ >
animation-duration: 0s <br />

애니메이션의 속도 곡선을 지정 <br />
animation-timing-function: ease <br />

딜레이 시간 이후 애니메이션 시작 <br />
animation-delay: 0s <br />

애니메이션 실행 횟수 설정 <br />
animation-iteration-count: 1 <br />

진행방향 (정방향, 역방향, 정방향 후 역방향, 역방향 후 정방향) <br />
animation-direction: normal <br />

애니메이션이 재생되지 않을 때, 요소에 대한 스타일을 지정 <br />
animation-fill-mode: none <br />

재생 상태 설정 <br />
animation-play-state: running <br />

OR <br />

하나로 합쳐서 사용하기 <br />
animation: example 5s linear 2s infinite alternate;

```
div {
  animation-name: example;
  animation-duration: 5s;
  animation-timing-function: linear;
  animation-delay: 2s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}

// 위에 있는걸 하나로 합치면 아래처럼 됨.

div {
  animation: example 5s linear 2s infinite alternate;
}
```