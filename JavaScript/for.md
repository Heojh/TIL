for
-

<br />

<h4>for...in</h4>
- 객체에 있는 항목들을 반복적으로 반환하여 '무언가'를 할 수 있게 해준다.
- 문법 : for (variable in object) { ... }
    - variable : 매번 반복마다 다른 속성이름(Value name)이 변수(variable)로 지정된다.
    - object : 반복작업을 수행할 객체로 열거형 속성을 가지고 있는 객체.
```
var o = {a: 1, b: 2, c: 3};
function showProps(obj, objName) {
    var result = '';
    for(var prop in obj) {
        result += `${objName}.${prop} = ${obj[prop]} \n`;
    }
    return result;
}
console.log(showProps(o, 'o'));

/* 
출력값
o.a = 1
o.b = 2
o.c = 3
*/
```
➕ 속성 접근자 : 점 또는 괄호 표기법으로 객체의 속성에 접근할 수 있도록 해준다.
- object.property
- object['property']

<br />

<h4>for...of</h4>
`for...of`명령문은 반복가능한 객체에 대해서 반복하고 각 개별 속성값에 대해 실행되는 문이 있는 사용자 정의 반복 후크를 호출하는 루프를 생성한다. <br />

<h5>Bulls and Cows</h5>

```
// 각 버튼마다 클릭이벤트가 실행될 수 있도록 함.
const btns = document.querySelectorAll('.btn')
for (const btn of btns) {
    btn.addEventListener('click', function(e) {
        const target = e.target;
        console.log(target.textContent);
    });
}
```