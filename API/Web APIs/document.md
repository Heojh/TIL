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
