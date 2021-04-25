# 📆 210426 질문

## JavaScript
### ES6 이후에 나온 문법 중, 유용한 문법은 무엇이 있는가?
  - Optional Chaining (ES11)
    - `?.` 연산자를 의미한다.
    - 아래와 같은 에러를 방지할 수 있다.
      ```javascript
      person.def.asd;
      // 에러
      VM370:1 Uncaught TypeError: Cannot read property 'asd' of undefined at <anonymous>:1:12
      ```
    - 참조한 property가 nullish(`null` 또는 `undefined`)라면 에러 대신 undefined를 리턴한다.
    - 참조한 property가 존재하면, 해당 값을 리턴한다.
    - 기존에 `삼항 연산자` 또는 `&&` 연산자로 에러를 방지할 수 있었다. 하지만 코드가 중복되거나 길어지는 단점이 존재했다. 이를 `?.`연산자를 이용해 해결할 수 있다. 
      ```javascript
        const person = {
          name: 'CCW',
          job: {
            title: 'Frontend Engineer',
            manager: {
              name: 'Fortuna'
            }
          }
        };

        // 문제의 코드
        const m1 = person.job && person.job.manager && person.job.manager.name;
        const m2 = person.job 
                    ? person.job.manager
                      ? person.job.manager.name
                      : undefined
                    : undefined

        // Optional Chaining
        const m3 = person?.job?.manager?.name;
      ```
  - Nullish Coalescing Operator (ES11)
    - Null 병합 연산자로 번역됨. 영어는 잘 이해가 안가는 말인듯.  
    - 왼쪽 피연산자가 `null` 또는 `undefined`일 때, 오른쪽 피연산자를 반환한다. 그렇지 않으면, 왼쪽 피연산자를 반환한다.
    - `||` 연산자와는 달리 `null`과 `undefined`말고 다른 `falsy`값은 반환된다. (`''` 또는 `0`)
    - 그런데, 만약 `falsy`값을 사용하도록 고려했다면 (`||`의 경우 오른쪽 피연산자를 반환하도록 했다면) `Null 병합 연산자`를 사용해선 안된다.  
      ```javascript
        const name1 = null ?? 'default string';
        console.log(name1); // 'default string';

        const name2 = '' ?? 'default string';
        console.log(name2); // ''

        // React jsx에서
        const imgUrl = '' ?? 'imgUrl2';
        <img src={imgUrl} ... /> // 이미지를 불러올 수 없어서 에러가 발생한다.
      ```

  
### 자바스크립트 콜백함수에 대해서 설명해보세요.

## 자율 카테고리
### atomic 디자인 패턴에 대해서 서로 알아보고 이야기해보기
### REST API에 대해서 설명해보세요.
3.
4. 
