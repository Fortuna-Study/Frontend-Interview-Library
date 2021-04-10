# 🐶 Week 3 질문 정리

## 📚 JavaScript

### 🎈 커링이란 무엇인가? 예제와 함께 설명하기
- https://ko.javascript.info/currying-partials

### 🎈 자바스크립트의 실행 컨텍스트에 대해서 설명하세요.
- 실행 컨텍스트는 실행할 코드에 제공할 환경 정보를 모아놓은 객체이다.
- 실행 컨텍스트는 전역 공간에서 자동으로 생성되는 전역 컨텍스트와 `eval` 및 함수 실행에 의한 컨텍스트 등이 있다.
- 실행 컨텍스트 객체는 활성화되는 시점에 `VariableEnvironment`, `LexicalEnvironment`, `ThisBinding`의 세 가지 정보를 수집한다.
- 실행 컨텍스트를 생성할 때는 `VariableEnvironment`와 `LexicalEnvironment`가 동일한 내용으로 구성하지만 `LexicalEnvironment`는 함수 실행 도중에 변경되는 사항이 즉시 반영되는 반면 `VariableEnvironment`는 초기 상태를 유지한다.
- `VariableEnvironment`와 `LexicalEnvironment`는 매개변수명, 변수의 식별자, 선언한 함수의 함수명 등을 수집하는 `environmentRecord`와 바로 직전 컨텍스트의 `LexicalEnvironment` 정보를 참조하는 `outerEnvironmentReference`로 구성돼 있다.
- 여기서 호이스팅이라는 개념을 알 수 있는데, 호이스팅은 코드 해석을 좀 더 수월하게 하기 위해 `environmentRecord`의 수집 과정을 추상화한 개념으로, 실행 컨텍스트가 관여하는 코드 집단의 최상단으로 이들을 끌어올린다라고 해석하는 것이다. 이때 변수 선언과 값 할당이 동시에 이뤄진 문장은 선언부만 호이스팅하고, 할당 과정은 원래 자리에 남아있게 되는데 여기서 함수 선언문과 함수 표현식의 차이가 발생한다.
- 스코프를 실행 컨텍스트 관점에서도 설명할 수 있는데, 스코프는 변수의 유효범위를 말한다. `outerEnvironmentReference`는 해당 함수가 선언된 위치의 `LexicalEnvironment`를 참조한다. 코드 상에서 어떤 변수에 접근하려고 하면 현재 컨텍스트의 `LexicalEnvironment`를 탐색해서 발견되면 그 값을 반환하고, 발견되지 못할 경우 다시 `outerEnvironmentReference`에 담긴 `LexicalEnvironment`를 탐색하는 과정을 거친다. 만약 전역 컨텍스트의 `LexicalEnvironment`까지 탐색해도 해당 변수를 찾지 못하면 `undefined`를 반환한다.

- [정리](https://github.com/saseungmin/reading_books_record_repository/tree/master/%EC%BD%94%EC%96%B4%20%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8/Chapter%202)

## 📚 자율 카테고리
### 🎈 JWT가 나오게 된 배경은?

### 🎈 클라이언트 사이드 렌더링과 서버 사이드 렌더링의 차이점
- https://asfirstalways.tistory.com/244