Web API > NodeList
-

<br />

<h4>NodeList.item()</h4>
NodeList의 node를 index로 돌려준다. <br />

<h5>**Project : Bulls and Cows**</h5>

```
// HTML
// 숫자 입력 버튼
<button class="btn number">1</button>
<button class="btn number">2</button>
<button class="btn number">3</button>
// ~ 4, 5, 6, 7, 8
<button class="btn number">9</button>
<button class="btn confirm">Confirm</button>
<button class="btn delete">Delete</button>
```

```
// JavaScript
const btns = document.querySelectorAll('.btn');
let arr = [];
for(let i = 0; i < btns.length; i++) {
    const item = btns[i]; // 👉 nodeItem = nodeList[index]
    console.log(item); // <button class="btn number">1</button> ~ 2,...,Confirm ~ Delete</button>
    arr.push(item.textContent);
}
console.log(item); // item is not defined
console.log(arr); // ["1","2", ... ,"9","Confirm","Delete"]
```