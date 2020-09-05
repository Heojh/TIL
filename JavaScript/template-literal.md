Template literal
-
ES6는 템플릿 리터럴(Template literal)이라고 불리는 새로운 문자열 표기법을 도입하였다. <br />
템플릿 리터럴은 일반 문자열과 비슷해 보이지만, ‘ 또는 “ 같은 통상적인 따옴표 문자 대신 백틱(backtick) 문자 `를 사용한다.

<br />

<h3>Cloning Styled Components</h3>

```
const styled = aElement => {
    const el = document.createElement(aElement);
    return args => {
        const styles = args[0];
        el.style = styles;
        return el;
    };
};

const title = styled('h1')` // use template literal
    background-color: red;
    color: blue;
`;

const subtitle = styled('span')` // use template literal
    color: green;
`;

title.innerText = 'We just cloned';
subtitle.innerText = 'Styled Components';

document.body.append(title, subtitle);
```