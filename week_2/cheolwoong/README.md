# 📆 210405 질문

## JavaScript
### 클로저에 대해서 설명하기
### 이벤트 버블링, 이벤트 캡처링, 이벤트 위임에 대해서 설명

## Web
### HTTP와 HTTPS의 차이점은?
### 쿠키(cookie)와 세션(session)의 차이점은?
  📌 참고
  - [쿠키(cookie)와 세션(session)의 개념/차이/용도/작동방식](https://devuna.tistory.com/23)
  - [쿠키와 세션 개념](https://interconnection.tistory.com/74)
### 브라우저 렌더링 과정을 설명해보세요.
  📌 참고
  - [브라우저의 렌더링 과정](https://velog.io/@st2702/%EB%B8%8C%EB%9D%BC%EC%9A%B0%EC%A0%80%EC%9D%98-%EB%A0%8C%EB%8D%94%EB%A7%81-%EA%B3%BC%EC%A0%95)
  - [브라우저 렌더링 과정 - Reflow Repaint, 그리고 성능 최적화](https://boxfoxs.tistory.com/408)
  
## React
### 리액트의 상태관리에 대해서 경험과 더불어 설명하라.
  - 경험한 상태관리
    - useState를 통한 컴포넌트 안에서의 상태 관리
    - redux를 통한 전역적인 상태 관리
    - redux-thunk와 redux-saga를 통한 미들웨어 관리
  - 상태관리를 이용한 예
    - 한 컴포넌트나 낮은 depth로 전달되는 상태는 useState 사용
    - 에러 확인 또는 API를 통한 상태관리에 주로 redux 사용
    - axios나 fetch를 통한 비동기처리 전후에 로직을 사용하기 위해 redux-thunk와 redux-saga를 사용
  - 들어본 상태관리 라이브러리
    - mobx, recoil
    - context API
    - redux-promise
  
### Redux-thunk와 Redux-saga를 비교해보세요.
  - 공통점
    두 라이브러리 모두, redux 미들웨어
  - 차이점
    thunk는 함수를 반환하여, 함수 내부에 추가적으로 로직을 실행한다.
    saga는 내부적으로 제너레이터로 구현되어 있고, 제너레이터 함수에 로직을 실행한다.
    
### React에서 컴포넌트 배열을 렌더링할 때 key를 사용하는 이유를 설명해보세요.
  - React는 Virtual DOM을 이용해서 변경이 일어나는 부분만 캐치해서 빠르게 화면을 렌더링하는 것을 목표로 한다.
  - 데이터 변경이 발생할 때, 변경이 일어나기 전의 DOM 트리와 변경이 일어난 후의 DOM 트리를 비교해서, 화면 변경을 처리한다.
  - key를 사용하지 않는다면, 엉뚱한 요소가 변경될 수 있다.
  - key에는 요소를 구별할 수 있는 unique한 값이 들어가야 한다. (id값)
  - key에 index값을 넣을 수도 있지만, 요소들의 위치가 변경될 때 index값도 바뀌므로 엉뚱한 요소가 변경되거나, 화면 재조정 시 불필요한 연산이 발생하여 성능적으로도 문제가 생긴다. O(1)으로 처리될 것이 O(n)으로 처리될 수 있다.
  
  📌 참고
  - [React에서 key는 어떤 역할을 할까요?](https://sgwanlee.medium.com/react%EC%97%90%EC%84%9C-key%EB%8A%94-%EC%96%B4%EB%96%A4-%EC%97%AD%ED%95%A0%EC%9D%84-%ED%95%A0%EA%B9%8C%EC%9A%94-9dcaead1b805)
  - [리스트와 Key](https://ko.reactjs.org/docs/lists-and-keys.html)
  - [재조정 (Reconciliation)](https://ko.reactjs.org/docs/reconciliation.html#recursing-on-children)
