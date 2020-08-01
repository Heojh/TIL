for
-

> for...in
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

<br/>

➕ 속성 접근자 : 점 또는 괄호 표기법으로 객체의 속성에 접근할 수 있도록 해준다.
- object.property
- object['property']