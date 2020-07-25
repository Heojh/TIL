REST
-

####Wiki :
a way of providing interoperability between computer systems on the internet.
👉 인터넷 상의 컴퓨터 시스템간에 상호 운용성을 제공하는 방법.

####History :
**1991 | WEB**
Q : 어떻게 인터넷에서 정보를 공유할 건인가?
A : 정보들을 하이퍼텍스트로 연결한다.
 - 표현방식 : HTML
 - 식별자 : URI
 - 전송방법 : HTTP
 
**1994-1996 | HTTP/1.0**
Roy T.Fielding : "How do I improve HTTP without breaking the Web?"
👉 해결책 : HTTP Object Model

**1998 | Roy T.Fielding, Microsoft Research에서 발표**
👉 REpresentational State Transfer : An Architectural Style for Distributed Hypermedia Interaction.

**2000 | REST**
Roy T.Fielding, 박사 논문으로 발표
👉 "Architectural Styles and the Design of Network-based Software Architectures"

---

###SOAP & REST
**1998 | XML-RPC(1998)**
👉 Microsoft에서 발표한 원격으로 다른 시스템의 메소드를 호출 할 수 있는 프로토콜이며 추후 SOAP라고 불린다.

**2000.2 | Salesforce API**
👉 Salesforce 회사에서 공개한 API, 인터넷에서 거의 최초로 공개된 API라고 볼 수 있다.
 ❗ 너무 복잡해서 인기가 없었다.

**2004.8 | flickr API**
👉 4년 후 flickr에서 SOPA API와 REST API를 발표
SOAP | REST
------------ | -------------
복잡하다 | 단순하다
규칙이 많다 | 규칙이 적다
어렵다 | 쉽다
❗ SOAP는 인기가 갈수록 추락하고, REST는 인기가 급상승 한다.

---

###What is REST API?
👉 REST 아키텍쳐 스타일을 따르는 API

###What is REST?
👉 분산 하이퍼미디어 시스템(ex: WEB)을 위한 아키텍쳐 스타일

###What is Architecture style?
👉 제약조건의 집합

###REST를 구성하는 스타일
- client-server
- stateless
- cache
- **uniform interface**
- layered system
- code-on-demand (optional) 👉 서버에서 코드를 클라이언트로 보내서 실행할 수 있어야 한다.(=JavaScript)
❗ 대체로 오늘날의 REST API는 잘 지켜지고 있는데, 그 이유는 HTTP만 잘 따라도 uniform interface를 제외한 조건들은 충족되기 때문이다.

###Uniform Interface의 제약조건
- identification resources
  - 리소스가 URI로 식별되면 된다.
- manipulation of resource through representations
  - 리소스를 삭제, 수정, 삽입 등을 할 때, HTTP 메세지에 표현을 담아서 전송해야 한다.
- **self-descriptive message** 
  - 메세지는 스스로를 설명해야 한다.
- **hypermedia as the engine of application state (HATEOAS)**
  - 애플리케이션의 상태는 Hyperlink를 이용해 전이되어야 한다.

###Why need a uniform interface?
👉 독립적 진화를 위해서
 - 서버와 클라이언트가 각각 독립적으로 진화한다.
 - 서버의 기능이 변경되어도 클라이언트를 업데이트 할 필요가 없다.
 - REST를 만들게 된 계기 : "How do I improve HTTP without breaking the Web?"

❗ 실제로 REST가 지켜지고 있는 사례 : WEB
- 웹 페이지를 변경했다고 웹 브라우저를 웹데이트 할 필요는 없다.
- 웹 브라우저를 업데이트 했다고 웹 페이지를 변경할 필요도 없다.
- HTTP 명세가 변경되어도 잘 동작한다.
- HTML 명세가 변경되어도 잘 동작한다.

❌ 모바일
- 모바일 앱 클라이언트와 서버가 REST 아키텍쳐 스타일을 따르고 있지 않다.

###REST가 웹의 독립적 진화에 도움을 주었나?
- HTTP에 지속적으로 영향을 줌
- Host 헤더 추가
- 길이 제한을 다루는 방법이 명시 (414 URI Too Long 등..)
- URI에서 리소스의 정의가 추상적으로 변경됨 : "식별하고자 하는 무언가"
- 기타 HTTP와 URI에 많은 영향을 줌
- HTTP/1.1 명세 최신판에서 REST에 대한 언급이 들어감
- Reminder : Roy T.Fielding이 HTTP와 URI 명세의 저자 중 한명이다.

###결론 : REST는 성공했는가?
- REST는 웹의 독립적 진화를 위해 만들어졌다. 👉 웹은 독립적으로 진화하고 있다.
- 성공👍

###REST API는?
- REST API는 REST 아키텍쳐 스타일을 따라야한다.
- 오늘날 스스로 REST API라고 하는 API들의 대부분이 REST 아키텍쳐 스타일을 따르지 않는다.

---

Reference : [그런 REST API로 괜찮은가](like https://www.youtube.com/watch?v=RP_f5dMoHFc&t=25s)
