<h3>배열의 요소 추출 및 추가</h3>

<h4>List</h4>
- .pop()
- .push()
- .shift()
- .unshift()
- .splice()
- .slice()

<br />

배열 생성

```
const numCandidate = [1,2,3,4,5,6,7,8,9,0];
const numPicked = [];
```

<br />

요소 추출 및 추가 -- 1

```
for(let i = 0; i < 5; i++) {
    const picked = numCandidate.pop(i); // .pop()
    numPicked.push(picked); // .push()
}
console.log(numCandidate); // [1,2,3,4,5]
console.log(numPicked); // [0,9,8,7,6]
```
`.pop()` 메서드는 배열에서 마지막 요소를 제거하고, 제거된 요소를 반환한다. <br />
`.push()` 메서드는 배열의 끝에 하나 이상의 요소를 추가하고, 새로운 길이를 반환한다. <br />

<br />

 추출 및 추가 -- 2

```
for(let i = 0; i < 5; i++) {
    const picked = numCandidate.shift();
    numPicked.unshift(picked);
}
console.log(numCandidate); // [6,7,8,9,0]
console.log(numPicked); // [5,4,3,2,1]
```
`.shift()` 메서드는 배열에서 첫 번째 요소를 제거하고, 제거된 요소를 반환한다.
`.unshift()` 메서드는 새로운 요소를 배열의 맨 앞쪽에 추가하고, 새로운 길이를 반환한다.