Web API > CSSOM
-

####What is CSSOM?
CSS 객체 모델(CSS Object Model, CSSOM)은 JavaScript에서 CSS를 조작할 수 있는 API 집합.
HTML 대신 CSS가 대상인 DOM이라고 생각할 수 있으며, 사용자가 CSS 스타일을 동적으로 읽고 수정할 수 있는 방법.

####Explain
- CSS cascading 규칙을 기반으로 스타일을 계산한다.
- 자식요소에서 스타일을 적용하지 않으면, 부모요소와 동일한 스타일을 가지게 된다.
- DOM + CSSOM = Render Tree

####Rendering order
1. 웹 브라우저는 HTML을 검사하고 DOM을 빌드
2. 웹 브라우저는 CSS를 검사하고 CSSOM을 빌드
3. 웹 브라우저는 DOM과 CSSOM을 결합하여 렌더 트리를 만든다.
4. 웹 브라우저에 웹 페이지가 표시된다.

