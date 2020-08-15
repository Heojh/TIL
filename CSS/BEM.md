BEM (Block, Element, Modifier)
-
- 웹 개발에 대한 구성 요소 기반 접근 방식.
- 사용자 인터페이스를 독립적인 블록으로 나누는 것.
- 이를 통해 복잡한 UI에서도 쉽고 빠르게 인터페이스를 개발할 수 있다.

<br />

<h4>Block</h4>
- 독립적으로 의미가 있는 구성요소(component)를 의미.
- 시멘틱 태그의 컨텐츠 영역을 `block`으로 간주할 수 있다.
- `block`은 클래스의 어근을 형성하고, 항상 맨 앞에 위치한다.

```
.block {
    background-color: red;
}
```

<br />

<h4>Element</h4>
- 독립적으로는 의미가 없으며 `block`에 붙여서 사용되는 구성요소를 의미.
- `element`는 `block`이 포함하고 있는 한 조각.

```
.block__element {
    background-color: orange;
}
```

<br />

<h4>Modifier</h4>
- `modifier`는 `block` 또는 `element`의 속성.
- 특정 요소의 스타일을 수정해야할 필요가 있을 때 `modifier`를 활용.

```
.block__element--modifier {
    background-color: yellow;
}
.header__button--red {
}
.header__button--green{
}
```