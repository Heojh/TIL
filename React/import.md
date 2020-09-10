<h3>Import</h3>

<h4>List</h4>
1. React <br />
2. ReactDOM <br />

<br /><br />

<h4>1. React</h4>
◾ 리액트 코어 라이브러리는 컴포넌트가 어떻게 작동하는지 알고있다. <br />
◾ 어떻게 렌더링 되며, 어떻게 그것들을 모으는지 등을 안다. (component를 생성하고 관리) <br />
◾ 'react'는 'react-dom'과 'react-native'의 지원을 받아 구동하게 된다. <br />
◾ 컴포넌트를 DOM에 렌더링하기 위해서는 'react'가 아닌 'react-dom'을 사용한다.

```
import React from 'react';

class App extends React.Component {
    ...
}
```

```
import React, { Component } from 'react';

class App extends Component {
    ...
}
```
{ Component } 의미 <br />
◾ React 라이브러리를 불러와 Component라 부르는 변수를 프로퍼티 형태로 가져오라는 것이다. <br />
◾ const Component = React.Component;를 나타낸다. <br />

<br />

<h4>2. ReactDOM</h4>
◾ 브라우저나 서버 환경에서 렌더링을 수행한다. <br />
◾ 실제로 DOM에 렌더링하는 기능을 가지고, 이 컴포넌트를 가져와 DOM에 삽입하는 라이브러리이다. (실제 DOM과 상호작용)

```
import ReactDOM from 'react-dom';

const rootNode = document.querySelector('.container');

ReactDOM.render(<App />, rootNode);
```

```
import { render } from 'react-dom';

const rootNode = document.getElementById('container');

render(<App />, rootNode);
```