Flexbox
-
flexbox는 행과 열의 형태로 항목 무리를 배치하는 일차원 레이아웃 메서드이다. <br />
항목은 부족한 공간에 맞추기 위해 축소되거나 여분의 공간을 채우기 위해 변형된다. <br />

<h4>주축과 교차축</h4>
flexbox를 다루려면 주축(main axis)과 교차축(cross axis)이라는 두 개의 축에 대한 정의를 알아야 한다. <br />
👉 main axis : flex item이 배치되고 있는 방향으로 진행하는 축. <br />
👉 cross axis : flex item이 내부에 배치되는 방향에 직각을 이루는 축. <br />

<br />

주축은 flex-direction에 의해 정의되며 4개의 값을 가질 수 있다. <br />
👉 주축이 인라인 방향으로 행을 따를 때 : row, row-reverse <br />
👉 주축이 페이지 상단에서 하단으로 블록 방향을 따를 때: column, column-reverse <br />

<br />

<h4>수평 및 추식 정렬</h4>
👉 justify-content : flex item의 주축 정렬을 제어. <br />
- flex-start
- flex-end
- center
- space-around
- space-between

👉 align-items : flex item의 교차축 정렬을 제어. <br />
- flex-start
- flex-end
- center