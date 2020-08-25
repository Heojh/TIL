Web API > Document
-
Document 인터페이스는 브라우저가 불러온 웹 페이지를 나타내며, 페이지 콘텐츠(DOM 트리)의 진입점 역할을 수행한다.

<br />

<h4>document.querySelector()</h4>
document.querySelector() 메소드는 제공한 선택자 또는 선택자 뭉치와 일치하는 문서 내 첫 번째 element를 반환한다.
일치하는 요소가 없으면 null을 반환한다.

```
// "select"라는 클래스를 사용하는 첫 번째 요소를 반환.
const element = document.querySelector('.select');

// "select"라는 ID를 사용하는 첫 번째 요소를 반환.
const element = document.querySelector('#select');

// <span> 태그를 사용하는 첫 번째 요소를 반환.
const tagSpan = document.querySelector('span');
```

<br />

<h4>document.querySelectorAll()</h4>
document.querySelectorAll() 메소드는 지정된 셀렉터 그룹에 일치하는 문서의 element list를 나타내는 정적 NodeList를 반환한다.
- querySelectorAll()로 가져오는 객체는 노드리스트인데 노트리스트란 element를 받아오는 메소드나 childNodes property의 값으로 반환되는 객체를 말한다.
- 노드리스트의 특징은 배열은 아니지만 인덱스로 접근이 가능하고, length property를 가지고 있는 유사배열객체라는 것이다. <br />

루프문을 이용해서 노드의 순서에 따라 alpha값을 균등하게 차이를 줌. <br />
밑으로 갈수록 그 값이 작아져서 글자가 투명해지도록 함.
```
// HTML
<p>HTML</p>
<p>CSS</p>
<p>JavaScript</p>
<p>Jquery</p>
<p>React</p>
<p>Node.js</p>

// JavaScript
const nodes = document.querySelectorAll('p');
let i = 0;
let alpha = 0;
while(i < nodes.length) {
    alpha = 1 - i / nodes.length;
    const colorValue = "rgba(0, 0, 255," + alpha + ")";
    nodes[i].style.color = colorValue;
    i++;
}
```