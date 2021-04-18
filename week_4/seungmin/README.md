# 🐶 Week 4 질문 정리

## 📚 JavaScript

### 🎈 this에 대해서 설명해주세요.
- `this`는 기본적으로 실행 컨텍스트가 생성될 때 함께 결정된다. 실행 컨텍스트는 함수를 호출할 때 생성되므로, `this`는 함수를 호출할 때 결정된다라고 할 수 있다. 그렇기에 `this`는 상황에 따라서 달라진다.
- 전역공간에서의 `this`는 전역객체를 참조하는데 브라우저에서는 window, Node.js에서는 global을 참조한다.
- 어떤 함수를 메서드로서 호출한 경우 `this`는 메서드 호출 주체를 참조한다. 즉, 메서드명 앞의 객체를 참조한다.
- 어떤 함수를 함수로서 호출한 경우 `this`는 전역객체를 참조한다. 이때 메서드의 내부함수에서도 `this`는 전역객체를 참조한다. 메서드의 내부함수에서 전역객체를 참조하는 것을 우회하는 방법으로는 내부에서 `self`라는 변수에 `this`를 저장하여 `self` 변수를 참조하여 상위 스코프의 `this`를 저장해서 활용할 수 있고 또 다른 방법은 `this`를 바인딩하지 않는 화살표함수를 사용할 수 있다.
- 콜백 함수 내부에서의 `this`는 해당 콜백 함수의 제어권을 넘겨받은 함수가 정의한 바에 따르며, 정의하지 않은 경우에는 전역객체를 참조한다.
- 생성자 함수에서의 `this`는 생성될 인스턴스를 참조한다.
- 또한, 명시적으로 `this` 바인딩할 수 있는데, `call`, `apply` 메서드는 `this`를 명시적으로 지정하면서 함수 또는 메서드를 호출한다. 둘은 기능적으로는 완전히 동일하나 차이점은 `apply`는 배열로 받아 그 배열 요소들을 호출할 함수의 매개변수로 지정한다.
- ES5에 추가된 `bind` 메서드는 `call`과 비슷하지만 즉시 호출하지 않고 넘겨받은 `this` 및 인수들을 바탕으로 새로운 함수를 반환하기만 하는 메서드이다. 그렇기 때문에 `bind` 메서드는 함수에 `this`를 미리 적용하는 것과 부분 적용 함수를 구현하는 두 가지 목적을 지닌다.
- 또한 `bind` 메서드를 적용해서 새로 만든 함수는 `name` 프로퍼티에 `bind`의 수동태인 `bound` 접두어가 붙는다. 그렇기 때문에 기존의 `call`이나 `apply`보다 코드를 추적하기에 더 수월해진다.
- 그리고 메서드의 내부함수에서 메서드의 `this`를 그대로 바라보게 하기 위한 방법으로 `call`, `apply` 또는 `bind` 메서드를 이용하여 `self`와 같은 변수를 할용하지 않을 수 있다.
- [this 정리 내용](https://github.com/saseungmin/reading_books_record_repository/tree/master/%EC%BD%94%EC%96%B4%20%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8/Chapter%203)
## 📚 자율 카테고리
### 🎈 swr을 사용해보고 특징 이야기하기 (axios, fetch와의 차이점 등...) <선택사항>

### 🎈 redux toolkit을 사용해보고 특징 이야기하기

### 🎈 CORS에 대해서 설명하세요.

#### 🐶 CORS란?
- Cross-Origin Resource Sharing(CORS)은 추가적인 HTTP header를 사용해서 애플리케이션이 다른 origin의 리소스에 접근할 수 있도록 해주는 메커니즘이다. 하지만 다른 [origin](https://developer.mozilla.org/en-US/docs/Glossary/Origin)에서 내 리소스에 함부로 접근하지 못하게 하기 위해 사용된다.
- 웹 애플리케이션은 리소스가 자신의 origin(도메인, 프로토콜, 포트)와 다를 때 Cross-Origin HTTP Request(교차 출처 HTTP 요청)를 실행한다.
- 브라우저는 스크립트에서 교차 출처 HTTP 요청을 제한한다. ([XMLHttpRequest](https://developer.mozilla.org/ko/docs/Web/API/XMLHttpRequest)와 [Fetch API](https://developer.mozilla.org/ko/docs/Web/API/Fetch_API)는 [동일 출처 정책(same-origin policy)](https://developer.mozilla.org/ko/docs/Web/Security/Same-origin_policy)을 따른다.) 즉, 이 API는 사용하는 웹 애플리케이션은 자신의 출처와 동일한 리소스만 불러올 수 있으며, **다른 출처의 리소스를 불러오면 그 출처에서 올바른 CORS 헤더를 포함한 응답을 반환해야 한다.**
- CORS 체제는 브라우저와 서버 간의 안전한 교차 출처 요청 및 데이터 전송을 지원한다.
- HTTP 요청 헤더
  - Origin: cross-site 접근 요청 또는 preflight request의 출처를 나타낸다.
  - Access-Control-Request-Method: 실제 요청에서 어떤 HTTP 메서드를 사용할지 서버에게 알려주기 위해, preflight request 할 때에 사용된다.
  - Access-Control-Request-Headers: 실제 요청에서 어떤 HTTP 헤더를 사용할지 서버에게 알려주기 위해, preflight request 할 때에 사용된다.

```
OPTIONS /resources/post-here/ HTTP/1.1
Host: bar.other
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.14; rv:71.0) Gecko/20100101 Firefox/71.0
...
Origin: http://foo.example
Access-Control-Request-Method: POST
Access-Control-Request-Headers: X-PINGOTHER, Content-Type
```

- HTTP 응답 헤더
  - Access-Control-Allow-Origin: 단일 출처를 ㄹ지정하여 브라우저가 해당 출처가 리소스에 접근하도록 허용한다. 또는 **자격 증명이 없는** 경우 `*` 와일드 카드는 브라우저의 origin에 상관없이 모든 리소스에 접근하도록 혀용한다.
  - Access-Control-Expose-Headers: 브라우저가 접근할 수 있는 헤더를 서버의 화이트리스트에 추가할 수 있다.
  - [Access-Control-Max-Age](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Max-Age): preflight request 요청 결과를 캐시할 수 있는 시간을 나타낸다.
  - Access-Control-Allow-Credentials: credentials 플래그가 true일 때 요청에 대한 응답을 표시할 수 있는지를 나타낸다. credentialed request 에 응답할 때 서버는 Access-Control-Allow-Origin 헤더 `*` 와일드카드를 사용하는 대신에 반드시 에 값을 지정해야 한다.
  - Access-Control-Allow-Methods: preflight request에 대한 대한 응답으로 리소스에 접근할 때 허용되는 메서드를 지정한다.
  - Access-Control-Allow-Headers: preflight request에 대한 대한 응답으로 실제 요청시 사용할 수 있는 HTTP 헤더를 나타낸다.

```
HTTP/1.1 204 No Content
Date: Mon, 01 Dec 2008 01:15:39 GMT
Server: Apache/2
Access-Control-Allow-Origin: https://foo.example
Access-Control-Allow-Methods: POST, GET, OPTIONS
Access-Control-Allow-Headers: X-PINGOTHER, Content-Type
Access-Control-Max-Age: 86400
Vary: Accept-Encoding, Origin
Keep-Alive: timeout=2, max=100
Connection: Keep-Alive
```

#### 🐶 CORS가 왜 필요할까?
- 만약 내가 서비스하고 있지 않은 사이트에서 세션을 요청해서 세션을 획득할 수 있다면 해당 사이트는 악의적으로 내 세션을 탈취하거나 다른 행동을 할 수 있다. 그래서 브라우저에서는 이러한 요청을 막는다. 피싱사이트가 대표적인 공격 사례인데 이러한 것을 막고 내가 허용한 origin들만 요청할 수 있도록 하기 위해 필요하다.

#### 🐶 CORS는 어떻게 동작할까?
- 브라우저가 리소스를 요청할 떄 추가적인 헤더에 정보를 담는다. 내 origin은 무엇이고 어떤 메소드를 사용해서 요청할 것이고, 어떤 헤더들을 포함할 것인지를 담아서 서버에 전송한다.
- 서버는 서버가 응답할 수 있는 origin들을 헤더에 담아서 브라우저에게 보낸다. 브라우저가 이 헤더를 보고 해당 origin에서 요청할 수 있다면 리소스 전송을 허용하고 만약 불가능하다면 에러를 발생시킨다.

#### 🐶 Reference
- https://developer.mozilla.org/ko/docs/Web/HTTP/CORS
- https://hannut91.github.io/blogs/infra/cors
