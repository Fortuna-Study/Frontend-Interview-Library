# 🐶 Week 1 질문 정리

## 📚 JavaScript
### 🎈 const와 var의 차이점은? (실행 컨텍스트 관점에서도 설명하기)

### 🎈 동기 처리와 비동기 처리의 차이점을 설명해보세요.

### 🎈 High Order Function(고차 함수)란 무엇인가?
- 고차 함수란 함수를 인자로 전달받거나 함수를 결과로 반환하는 함수를 말한다.
- 고차 함수는 인자로 받은 함수를 필요한 시점에 호출하거나 클로저를 생성하여 반환한다. 이때 자바스크립트의 함수는 일급 객체이기 때문에 값처럼 인자로 전달할 수 있으며 반환할 수도 있다. 
- 고차 함수는 기본적으로 외부 상태 변경이나 가변 데이터를 피하고 불변성을 지향하는 함수형 프로그래밍에 기반을 두고 있다.
- `Array`의 `map`, `filter`, `reduce`메서드 등이 있다.
- 예제
```js
function makeCounter(predicate) {
  let num = 0;
  // 클로저. num의 상태를 유지한다.
  return function () {
    num = predicate(num);

    return num;
  };
}

function increase(num) {
  return num += 1;
}

function decrease(num) {
  return num -= 1;
}

// 함수를 인자로 받고, 클로저를 반환한다.
const increaser = makeCounter(increase);
increaser(); // 1
increaser(); // 2

const decreaser = makeCounter(decrease);
decreaser(); // -1
decreaser(); // -2
```

- [📌 참고](https://poiemaweb.com/js-array-higher-order-function)

## 📚 Web
### 🎈 웹 브라우저 url에 www.naver.com 를 입력했을 때, 화면이 나오기까지 일어나는 일을 설명해라.

### 🎈 프레임워크와 라이브러리의 차이점
- 프레임워크는 말그대로 뼈대나 기반구조를 뜻하고 라이브러리는 도구들의 집합으로써 둘의 차이점은 **제어 흐름에 대한 주도성이 누구에게/어디에** 있는가에 있다. 즉, 애플리케이션의 흐름을 누가 쥐고 있느냐에 달려 있다.
- 프레임워크는 전체적인 흐름을 스스로가 쥐고 있으며 사용자는 그 안에서 필요한 코드를 짜 넣는다. (가져다 사용한다기보다 거기에 들어가서 사용한다는 느낌)
- 라이브러리는 사용자가 전체적인 흐름을 만들며 라이브러리를 가져다 쓰는 것.
- 즉, 프레임워크는 애플리케이션의 코드는 짜놓은 틀에서 수동적으로 동작해야 하며(제어의 역전), 라이브러리를 사용하는 애플리케이션 코드는 애플리케이션 흐름을 직접 제어한다.
- 간단하게 정리하면 라이브러리는 함수들이나 기능 모음을 가져다가 쓰는 것이고, 프레임워크느는 특정 디자인 패턴이나, 전처리 후처리에 필요한 동작과 기능들을 수행하기 위해서 프레임워크가 실행되다가 중간 중간에 특정 비지니스나, 특정 구현 단에서만 사용자의 코드를 lookup(검색)하여 사용하는 형태이다.

> **👉 예**
> - 라이브러리는 톱, 망치, 삽같은 연장이다. 즉, 사람이 톱을 썰다가, 망치로 바꿔서 내려칠 수도 있고, 삽으로 땅을 팔 수도 있다. 도구를 **선택하는 입장**이기 떄문에 어떤 도구를 사용하든 원하는 것을 만들어낼 수만 있으면 된다.
> - 프레임워크는 차, 비행기 배같은 탈 것이라고 할 수 있다. 탈 것은 정해진 곳으로만 다녀야 한다. 즉, 차를 타고 하늘을 날거나, 배를 타고 땅으로 갈 수는 없다. 하지만, 그 **목적에 맞게** 만들어져 있기 때문에, 톱이나 망치를 들고 탈 것을 만들어야 할 필요가 없다. 그저 정해진 규칙에 맞춰서 엔진, 기어, 핸들만 잘 돌리면 된다.

- [📌 참고](https://webclub.tistory.com/458)

### 🎈 크로스 브라우징 이슈에 대응하는 방법을 설명해주세요.

## 📚 React
### 🎈 useCallback은 언제 사용하는가?
### 🎈 클래스형 컴포넌트와 함수형 컴포넌트의 차이는 무엇인가?
### 🎈 JSX란?
- JavaScript 확장 문법으로 JSX는 중괄호에 모든 유효한 JavaScript 표현식을 넣을 수도 있고, JSX 조차도 표현식이다.
- Babel의 컴파일 과정이 끝나면 JSX 표현식이 JavaScript 함수 호출이 되고 JavaScript 객체로 인식된다. 즉, JSX를 `if` 구문 및 `for` loop 안에 사용하고, 변수에 할당하고, 인자로서 받아들이고, 함수로부터 반환할 수 있다.

```jsx
function getGreeting(user) {
  if (user) {
    return <h1>Hello, {formatName(user)}!</h1>;
  }
  return <h1>Hello, Stranger.</h1>;
}

// Babel은 JSX를 React.createElement 호출로 컴파일한다.
function getGreeting(user) {
  if (user) {
    return /*#__PURE__*/_react.default.createElement("h1", null, "Hello, ", formatName(user), "!");
  }

  return /*#__PURE__*/_react.default.createElement("h1", null, "Hello, Stranger.");
}
```

- React는 별도의 파일에 마크업과 로직을 넣어 기술을 인위적으로 분리하는 대신, 둘 다를 포함하는 컴포넌트라고 부르는 느슨하게 연결된 유닛으로 관심사를 분리한다. 이를 위해 사용하는 것이 JS에 마크업을 넣을 수 있게 해주는 JSX문법이다.

- [📌 참고](https://ko.reactjs.org/docs/introducing-jsx.html) 