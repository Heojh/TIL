Number
-
- path : JavaScript reference > Standard built-in objects > Number

<h4>Number.prototype.toLocaleString()</h4>
- 숫자 3자리 단위마다 콤마(comma) 찍기
```
for(let i=1; i < 10; i++) {
    const num = 10**i;
    console.log(num.toLocaleString());
}
```
출력 : <br />
"10" <br />
"100" <br />
"1,000" <br />
"10,000" <br />
"100,000" <br />
. <br />
. <br />
"1,000,000,000" 
