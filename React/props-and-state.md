<h3>Props and State</h3>

<h4>List</h4>
1. props <br />
2. state <br />

<br /><br />

<h4>1. props</h4>
◾ 리액트 컴포넌트에서 다루는 데이터는 props와 state이다. <br />
◾ props는 부모 컴포넌트가 자식 컴포넌트에게 주는 값이다. <br />
◾ 자식 컴포넌트에서는 props를 받아오기만 하고, 받아온 props를 직접 수정할 수 없다. <br />
◾ state는 컴포넌트 내부에서 선언하며 내부에서 값을 변경할 수 있다. <br />

<br />

<h4>2. state</h4>
◾ 동적인 데이터를 다룰 때 사용한다. <br />
◾ 컴포넌트의 state를 정의할 때는 Class field 문법을 사용해서 정의한다.

```
class App extends Component {
    state = { name: 'heojh' };
    render() {
        return <div>{this.state.name}</div>;
    }
}
```

◾ class field 문법을 사용하지 않는다면 constructor를 정의하고 super(props)를 호출하여 사용한다.

```
class App extends Component {
    constructor(props) {
        super(props);
        this.state = { name: 'heojh' };
    }
    render() {
        return <div>{this.state.name}</div>;
    }
}
```

<h5>2-1.super()</h5>
◾ 리액트 컴포넌트 내에서 constructor를 쓰면 그 안에 꼭 super()를 써주어야 한다. <br />
◾ this가 초기화되어서 super()를 넣지 않으면 Missed superclass's constructor invocation 에러가 발생한다. <br />
◾ this를 사용하기 전에 super()를 적어놓지 않으면 'this' is not allowed before super() 에러가 발생한다. <br />
◾ 이유는 super()를 넣어주지 않으면 this가 초기화되지 않기 때문이다. <br />

<h5>2-2.super() and super(props)</h5>
◾ constructor에서 props를 사용 한다면 props를 넘겨주고, 그렇지 않으면 아무것도 넘기지 않는다. <br />
◾ 또한, constructor가 아닌 다른 곳에서 props를 사용할 것 이라면 props를 넘겨줄 필요가 없다. react가 알아서 세팅해 주기 때문이다.