DOM 요소 선택
-
자바스크립트에서 특정 HTML 요소를 선택하는 방법은 다음과 같다.

1. HTML 태그 이름(tag name)을 이용한 선택.
2. 아이디(id)를 이용한 선택.
3. 클래스(class)를 이용한 선택.
4. name 속성(attribute)을 이용한 선택.
5. CSS 선택자(selector)을 이용한 선택.
6. HTML 객체 집합(object collection)을 이용한 선택.

<br>

<h4>HTML 태그 이름(tag)을 이용한 선택</h4>
getElementsTagName() <br>
▶ 태그를 가지고 있는 모든 요소를 선택함으로 getElement + s
```
// 모든 <li> 요소를 선택함.
const list = document.getElementsByTagName('li');

// 선택된 모든 요소의 텍스트 생상을 변경함.
for(let i = 0;, i < list; i++) {
	list.item(i).style.color = 'red';
}
```

<br>

<h4>아이디(id)를 이용한 선택</h4>
getElementById() <br>
▶ 고유식별자이므로 getElement 에 s 가 붙지 않는다.
```
// 아이디가 'itemId'인 요소를 선택함.
const selectedItem = document.getElementById('itemId');

// 선택된 요소의 텍스트 생상을 변경함.
selectedItem.style.color = 'red';
```

<br>

<h4>클래스(class)를 이용한 선택</h4>
getElementsClassName() <br>
▶ 클래스를 가지고 있는 모든 요소를 선택하므로 getElement + s
```
// 클래스가 'itemClass'인 모든 요소를 선택함.
const selectedItem = document.getElementsByClassName('itemClass');

// 선택된 모든 요소의 텍스트 색상을 변경함.
for(let i = 0; i < selectedItem; i++) {
	selectedItem.item(i).style.color = 'red';
}
```

<br>

<h4>name 속성을 이용한 선택</h4>
getElementsByName()
```
// name 속성값이 'itemName'인 모든 요소를 선택함.
const selectedItem = document.getElementsByName('itemName');

// 선택된 모든 요소의 텍스트 색상을 변경함.
for(let i = 0; i < selectedItem; i++) {
	selectedItem.item(i).style.color = 'red';
}
```

<br>

<h4>CSS 선택자(selector)를 이용한 선택</h4>
querySelector() <br>
- 반환객체는 한 개의 요소만 찾을 수 있으며 동일한 클래스명을 가진 객체가 있을 경우 html문서내의 첫 번째를 나타내는 요소를 반환한다. <br>

querySelectorAll()
- 해당 선택자에 해당하는 모든 요소를 가져온다.
- 반환객체는 nodeList이기 때문에 for문 또는 foreach 문을 사용해야 한다.
```
// <li> 요소중에서 클래스가 'itemClass'인 요소를 선탁함.
const selectedItem = document.querySelectorAll('li.itemClass');

// 선택된 모든 요소의 텍스트 색상을 변경함.
for(let i = o; i < selectedItem; i++) {
	selected.item(i).style.color = 'red';
}
```
▶ CSS 선택자 : 아이디, 클래스, 속성, 속성값 등 <br>

<br>

<h4>HTML 객체 집합(object collection)을 이용한 선택</h4>
HTML DOM에서 제공하는 객체 집합(object collection)을 이용하여 HTML요소를 선택할 수 있다.
```
// <title> 요소를 선택함.
const title = document.title;
document.write(title);
```
