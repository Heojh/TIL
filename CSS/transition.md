Transition
- 
- CSS 프로퍼티의 값이 변화할 때, 프러퍼티 값의 변화가 일정 시간(duration)에 걸쳐 일어나도록 하는 것
- 상태 변화에 따라 CSS 프로퍼티가 변경되면 프로퍼티 변경에 따른 표시의 변화(transition)는 지체없이 즉시 발생

<br />

<h4>transition</h4>
- 해당 요소에 추가할 CSS 스타일 전환 효과를 설정
- 추가할 전환 효과가 지속될 시간을 설정

<br />

<h4>transition-delay</h4>
- 전환 효과가 나타나기 전까지의 지연 시간을 설정
- 전환 효과는 설정된 시간이 흐른 뒤에 시작

<br />

<h4>transition-duration</h4>
- 전환 효과가 지속될 시간을 설정

<br />

<h4>transition-property</h4>
- 요소에 추가할 전환 효과를 설정

<br />

<h4>transition-timing-function</h4>
- 전환 효과의 시간당 속도를 설정
    - linear : 전환 효과가 처음부터 끝까지 일정한 속도로 진행
    - ease : default 값. 전환 효과가 천천히 시작되어 빨라진 후 마지막에는 느려짐
    - ease-in : 전환 효과가 천천히 시작
    - ease-out : 전환 효과과 천천히 끝남
    - ease-in-out : 전환 효과가 천천히 시작되고, 천천히 끝남
    - cubic-bezier(num, num, num, num) : 전환 효과가 사용자가 정의한 cubic-bezir 함수에 따라 진행