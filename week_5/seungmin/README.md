# 🐶 Week 5 질문 정리

## 📚 JavaScript

### 🎈 ES6 이후에 나온 문법 중, 유용한 문법은 무엇이 있는가?

### 🎈 자바스크립트 콜백함수에 대해서 설명해보세요.

## 📚 자율 카테고리

### 🎈 atomic 디자인 패턴에 대해서 서로 알아보고 이야기해보기

### 🎈 REST API에 대해서 설명해보세요.

#### 🐶 REST란?
- REpresentational State Transfer의 약자
- 전반적인 웹 어플리케이션에서 상호작용하는데 사용되는 웹 아키텍쳐 모델이다. 
- 즉, 자원을 주고받는 웹 상에서의 통신 체계에 있어서 범용적인 스타일을 규정한 아키텍쳐

#### 🐶 API란?
- Application Programming Interface의 약자
- 구글 맵 API, 카카오 맵 API 등 기존에 있는 응용 프로그램을 통해서 데이터를 제공받거나 기능을 사용하고자 할 때 사용하는 인터페이스 및 규격을 말한다.
- REST API라는 것은 REST 원칙을 적용하여 서비스 API를 설계한 것을 말하며 대부분의 서비스가 REST API를 제공한다.

#### 🐶 REST의 특징
1. 균등한 인터페이스
    - REST가 HTTP의 표준만 따른다면 어떠한 기술이던지 접목하여 사용할 수 있기 때문에 플랫폼이나 언어의 제약에 구애받지 않는다. 요즘은 REST API를 정의할 때 JSON 방식을 가장 많이 사용하지만 XML도 적용가능하다.
2. 무상태성
    - 서버는 클라이언트의 상황을 고려하지 않고 API 요청에 대해서만 처리하기 때문에 이를 **상태가 없다** 라고 표현한다. 이렇게 되면 클라이언트를 고려하지 않아도 되기 때문에 구현이 간결해진다.
3. 캐싱 가능
    - REST는 HTTP 표준을 기반으로 만들어졌기 때문에 HTTP의 특징인 캐싱을 사용할 수 있다. REST API를 활용하여 `GET` 메소드를 `Last-Modified` 값과 함께 보낼 경우, 컨텐츠의 변화가 없을 때 캐시된 값을 사용하게 된다.
4. 자체 표현성
    - REST API의 자원명시 규칙 및 메소드는 그 자체로 의미를 지니기 때문에 어떠한 요청에 있어서 그 요청 자체로 어떤 것을 표현하는지 알아보기 쉽다.
5. 클라이언트-서버 구조
    - REST 서버가 API를 제공하는 방식이기 때문에 클라이언트에서 처리하는 부분과 독립적으로 동작한다. 따라서, 서로간의 의존성이 줄어들고 클라이언트와 서버를 최대한 독립적으로 개발할 수 있도록 도와준다.
6. 계층형 구조
    - REST 서버의 경우, 보안/로드 밸런싱/암호화 등을 추가할 수 있고 Proxy 및 게이트웨이 등의 중간매체를 사용할 수 있다.

#### 🐶 REST API의 핵심
1. URI는 정보의 자원(리소스)을 표현해야 한다.

리소스 명은 동사가 아닌 명사를 사용해야 한다.

```
/students/1
```

리소스는 `Collection`과 `Document`로 표현할 수 있다. 이때 `Collection`은 복수를 사용해야 한다. (`locations`은 `Collection`, `seoul`은 `Document`)

```
/locations/seoul/schools/3
```

1. 자원에 대한 행위는 HTTP Method(GET, POST, PUT, DELETE)로 표현한다.

`GET`은 리소스를 조회한다.

```
GET /members
```

`POST`는 리소스를 생성한다.

```
POST /members
```

`PUT`는 리소스를 업데이트한다.

```
PUT /members/1
```

`DELETE`는 리소스를 삭제한다.

```
DELETE /members/1
```

#### 🐶 URI 설계 시 주의할 점
- 슬래시 구분자(/)는 계층 관계를 나타내는 데 사용한다.
- URI 마지막 문자로 슬래시(/)를 포함하지 않는다.

```
http://restapi.example.com/members/apartments/ (X)
http://restapi.example.com/members/apartments  (0)
```

- 하이픈(-)은 URI 가독성을 높이는데 사용
- 밑줄(_)은 URI에 사용하지 않는다.
- URI 경로에는 소문자가 적합하다.
- 파일 확장자는 URI에 포함시키지 않는다.

#### 🐶 HTTP 상태 코드
요청에 대한 응답의 상태코드 또한 명확하게 돌려주는 것이 잘 설계된 REST API이다.

- 2xx : 성공 관련 (200 Ok, 201 Created)
- 3xx : 리다이렉션 관련 (304 Not Modified)
- 4xx : 클라이언트 에러 관련(400 Bad Request, 401 Unauthorized)
- 5xx : 서버 에러 관련 (500 Internal Server Error)

#### 🐶 Reference
- https://meetup.toast.com/posts/92
- https://github.com/baeharam/Must-Know-About-Frontend/blob/master/Notes/network/rest-api.md
