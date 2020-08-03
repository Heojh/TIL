CSS > Media Queries
-

<h3>미디어 쿼리</h3>
미디어 쿼리는 '미디어 타입'과 적어도 하나 이상의 표현식(expression)으로 구성된다. <br />
표현식은 width, height, color와 같은 '미디어 특성'들을 이용하여 그 특성들의 상태에 따라 다른 스타일 시트를 적용할 수 있다. <br />
미디어 쿼리는 컨텐츠의 변경없이 주로 화면의 크기에 따라 스타일 시트를 달리하여 적절한 모양을 보여줄 수 있다.

<h4>사용 방법</h4>
1. `<link>`요소에 사용하여 특성이 조건에 맞을 때 CSS 파일을 불러온다. <br />
 media속성의 `screen and (max-width: 768px)`의 의미는 미디어 타입이 스크린이고, 화면의 최대 너비를 768px로 지정하는 것이다. 
 즉, 화면의 너비가 768px 이하 일 때 적용이 된다.
 
2. 스타일 시트내에서 @media를 사용한다. 결과는 위와 동일한 조건이고, 그 조건이 맞으면 {...} 안의 스타일이 적용된다.
```
@media screen and (max-width: 768px) {
    body {
        background-color: orange;
    }
}
```
`@media (max-width: 768px) {...}`처럼 미디어 타입을 생략하면 all이 default값이 되어 모든 미디어 타입에 적용된다.
