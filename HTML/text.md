textContent / innerText / innerHTML
-

[textContent, innerText]
- 지정된 노드의 텍스트 내용과 모든 하위 항목을 설정하거나 반환한다.
- 속성을 설정하면 모든 자식노드가 제거되고 지정된 문자열이 포함된 단일 Text노드로 대체된다.

[innerText와 textContent의 차이점]
- textContent는 모든 요소의 텍스트 내용을 반환하고,
- innerText는 script 및 style 요소를 제외한 모든 요소의 내용을 반환한다.
    > ❗ innerText는 CSS로 숨겨진 요소의 텍스트를 반환하지 않는다.

[innerHTML]
- 요소의 HTML 내용을 설정하거나 반환한다.
