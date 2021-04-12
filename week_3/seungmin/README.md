# 🐶 Week 3 질문 정리

## 📚 JavaScript

### 🎈 커링이란 무엇인가? 예제와 함께 설명하기
- https://ko.javascript.info/currying-partials

### 🎈 자바스크립트의 실행 컨텍스트에 대해서 설명하세요.
- 실행 컨텍스트는 실행할 코드에 제공할 환경 정보를 모아놓은 객체인데 실행 컨텍스트는 전역 공간에서 자동으로 생성되는 전역 컨텍스트와 `eval` 및 함수 실행에 의한 컨텍스트 등이 있다.
- 실행 컨텍스트 객체는 활성화되는 시점에 `VariableEnvironment`, `LexicalEnvironment`, `ThisBinding`의 세가지 정보를 수집한다.
- 실행 컨텍스트를 생성할 때는 `VariableEnvironment`, `LexicalEnvironment`가 동일한 내용으로 구성하지만 `VariableEnvironment`는 초기 상태를 유지한다.
- `VariableEnvironment`와 `LexicalEnvironment`는 매개변수명, 변수의 식별자, 선언한 함수의 함수명 등을 수집하는 `environmentRecord`와 바로 직전 컨텍스트의 `LexicalEnvironment` 정보를 참조하는 `outerEnvironmentReference`로 구성돼 있다.
- 여기서 호이스팅이라는 개념을 얘기할 수 있는데, 일단 호이스팅은 코드 해석을 좀 더 수월하게 하기 위해 이들을 끌어올린다라고 해석하는 것이다. 이때 변수 선언과 값 할당이 동시에 이뤄진 문장은 선언부만 호이스팅하고, 할당 과정은 원래 자리에 남아있게 된다. 
- 여기서 함수 선언문과 함수 표현식의 차이가 발생하게 되는데 함수 선언문은 함수 자체를 호이스팅하고 함수 표현식은 함수 표현식은 식이기 때문에 선언부만 호이스팅 된다. 때문에 함수 표현식이 좀 더 안전하다고 볼 수 있다.
- `outerEnvironmentReference`는 해당 함수가 선언된 위치 `LexicalEnvironment`를 참조한다. 코드 상에서 어떤 변수에 접근하려고 하면 해당 컨텍스트의 `LexicalEnvironment`를 탐색해서 발견이 되면 그 값을 반환하고, 발견되지 못했을 경우는 다시 `outerEnvironmentReference`에 담긴 `LexicalEnvironment`를 탐색하는 과정을 거치는데 이 과정을 스코프 체인이라고 한다. 이때 만약 전역 컨텍스트의 `LexicalEnvironment`까지 탐색해도 해당 변수를 찾지 못하면 `undefined`를 반환한다. 
- 이런 구조적인 특성 덕분에 여러 스코프에서 동일한 식별자를 선언한 경우에는 무조건 스코프 체인 상에서 가장 먼저 발견된 식별자에만 접근이 가능하게 되는 것이다.
- `ThisBinding`에는 `this`로 지정된 객체가 저장된다. 실행 컨텍스트 활성화 당시에 `this`가 지정되지 않은 경우 `this`는 전역 객체가 저장된다. 그밖에는 함수를 호출하는 방법에 따라 `this`에 저장되는 대상이 다르다.
- [정리](https://github.com/saseungmin/reading_books_record_repository/tree/master/%EC%BD%94%EC%96%B4%20%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8/Chapter%202)

## 📚 자율 카테고리
### 🎈 JWT가 나오게 된 배경은?
- 서버에서는 사용자에 대한 세션을 유지 할 필요가 없어진다. 즉 사용자가 로그인되어있는지 안되어있는지 신경 쓸 필요가 없고, 사용자가 요청을 했을때 토큰만 확인하면 되므로 세션 관리가 필요 없어서 서버 자원과 비용을 절감할 수 있다.
- [프론트에서 안전하게 로그인 처리하기](https://velog.io/@yaytomato/%ED%94%84%EB%A1%A0%ED%8A%B8%EC%97%90%EC%84%9C-%EC%95%88%EC%A0%84%ED%95%98%EA%B2%8C-%EB%A1%9C%EA%B7%B8%EC%9D%B8-%EC%B2%98%EB%A6%AC%ED%95%98%EA%B8%B0)

### 🎈 클라이언트 사이드 렌더링과 서버 사이드 렌더링의 차이점
- https://asfirstalways.tistory.com/244
