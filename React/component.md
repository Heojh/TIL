<h3>Component</h3>

<h4>List</h4>
1. 컴포넌트란? <br />
2. 함수형 컴포넌트 <br />
3. 클래스 기반 컴포넌트 <br />
4. 컴포넌트와 관련해서 2가지 할 일 <br />
5. 컴포넌트 생성 <br />
6. 컴포넌트 연습 <br />
7. 컴포넌트 클래스 VS 컴포넌트 인스턴스 <br />

<br /><br />

<h4>1. 컴포넌트란?</h4>
◾ Component : 구성요소 <br />
◾ 기능을 단위별로 캡슐화하는 리액트의 기본단위이다. <br />
◾ 사용자가 보는 뷰는 이 컴포넌트들을 조합하여 만든다. <br />
◾ 속성들의 이력을 받아들이며, 내부적으로는 각자의 상태를 관리한다. <br />

<br />

<h4>2. 함수형 컴포넌트</h4>
◾ 단순히 props와 state에서 받은 자료를 사용자에게 보여줄 때 사용된다. <br />
◾ 하나의 함수가 JSX(JavaScript XML) 형태를 반환한다.

```
const App = () => {
    return <div>Hello!</div>;
};
```

<br />

<h4>3. 클래스 기반 컴포넌트</h4>
◾ 라이프사이클과 다양한 이벤트를 구현할 때 필요하다. <br />
◾ 내부적인 정보를 저장하려고 할 때 사용된다. <br /> 
◾ state를 파악할 필요가 있을 때 사용된다.

```
class App extends Component {
    render() {
        return <div>Hola!</div>;
    }
}
```

<br />

<h4>4. 컴포넌트와 관련해서 2가지 할 일</h4>
◾ Create a new Component. This component should produce some HTML. <br />
-> 새로운 컴포넌트 생성. 이 컴포넌트는 HTML을 생성하게 될 것이다. <br />

<br />

◾ Take this component's generated HTML and put it on the page. (in the DOM) <br />
-> 컴포넌트가 만든 HTML을 가져오고 페이지에 반영한다. (DOM 안에) <br />

<br />

<h4>5. 컴포넌트 생성</h4>
◾ 디자인을 살펴보고 어떻게 컴포넌트를 나눌 것인지 기획한다. <br />
◾ API가 애플리케이션에 어떤 데이터를 제공해 주는지 파악한다. <br />
◾ 컴포넌트는 DOM 요소들처럼 중첩할 수 있으며 다른 컴포넌트를 포함할 수도, 옆에 배치할 수도 있다. <br />

<br />

<h4>6. 컴포넌트 연습</h4>
◾ 컴포넌트를 적절하게 그룹화한다. <br />
◾ 컴포넌트는 서로 관련된 기능을 제공하는 것들로 구성해야 한다. <br />
◾ 컴포넌트를 자유롭게 배치하기 어렵다면 아마도 계층구조를 너무 견고하게 정의했을 가능성이 있다. <br />
◾ 인터페이스의 어떤 요소가 여러번 반복되어 나타난다면 이런 요소들은 컴포넌트로 정의하면 좋다. <br />

<br />

<h4>7. 컴포넌트 클래스 VS 컴포넌트 인스턴스</h4>

◾ ReactDOM.render(App) : Component class

```
ReactDOM.render(App); // -> error
```

<br />

◾ ReactDOM.render(<App />) : Component instance

```
ReactDOM.render(<App />; // -> OK
```

<br />

❗ Error<br />
-> Invariant Violation: ReactDOM.render( ): Invalid component element. <br />
Instead of passing a component class, make sure to instantiate it by passing it to React.createElemet. <br />
-> 잘못된 구성 요소입니다. 컴포넌트 클래스를 전달하는 대신 React.createElemet에 전달하여 인스턴스화해야합니다. <br />