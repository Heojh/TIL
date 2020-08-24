Loops and Iteration : 루프와 반복
-

<h4>for문과 while문의 차이</h4>
`for`문을 사용하는 경우 <br />
👉 반복 횟수를 이미 알고 있을 때만 사용.

```
// 구구단
for(let i = 2; i <= 9; i++) {
    console.log(`${i}단`);
    for(let j = 1; j <= 9; j++) {
        console.log(`${i} X ${j} = ${i*j}`);
    }
}
```

<br />

`while`문을 사용하는 경우 <br />
👉 반복 횟수를 정확히 알 수 없는 경우에만 사용.

```
let sum = 0;
let i = 1;
while(i <= 10) {
    sum += i;
    i++;
}
console.log(`1 ~ ${i-1} 합은 ${sum}`); // 55
```