# πΆ Week 4 μ§λ¬Έ μ λ¦¬

## π JavaScript

### π thisμ λν΄μ μ€λͺν΄μ£ΌμΈμ.
- `this`λ κΈ°λ³Έμ μΌλ‘ μ€ν μ»¨νμ€νΈκ° μμ±λ  λ ν¨κ» κ²°μ λλ€. μ€ν μ»¨νμ€νΈλ ν¨μλ₯Ό νΈμΆν  λ μμ±λλ―λ‘, `this`λ ν¨μλ₯Ό νΈμΆν  λ κ²°μ λλ€λΌκ³  ν  μ μλ€. κ·Έλ κΈ°μ `this`λ μν©μ λ°λΌμ λ¬λΌμ§λ€.
- μ μ­κ³΅κ°μμμ `this`λ μ μ­κ°μ²΄λ₯Ό μ°Έμ‘°νλλ° λΈλΌμ°μ μμλ window, Node.jsμμλ globalμ μ°Έμ‘°νλ€.
- μ΄λ€ ν¨μλ₯Ό λ©μλλ‘μ νΈμΆν κ²½μ° `this`λ λ©μλ νΈμΆ μ£Όμ²΄λ₯Ό μ°Έμ‘°νλ€. μ¦, λ©μλλͺ μμ κ°μ²΄λ₯Ό μ°Έμ‘°νλ€.
- μ΄λ€ ν¨μλ₯Ό ν¨μλ‘μ νΈμΆν κ²½μ° `this`λ μ μ­κ°μ²΄λ₯Ό μ°Έμ‘°νλ€. μ΄λ λ©μλμ λ΄λΆν¨μμμλ `this`λ μ μ­κ°μ²΄λ₯Ό μ°Έμ‘°νλ€. λ©μλμ λ΄λΆν¨μμμ μ μ­κ°μ²΄λ₯Ό μ°Έμ‘°νλ κ²μ μ°ννλ λ°©λ²μΌλ‘λ λ΄λΆμμ `self`λΌλ λ³μμ `this`λ₯Ό μ μ₯νμ¬ `self` λ³μλ₯Ό μ°Έμ‘°νμ¬ μμ μ€μ½νμ `this`λ₯Ό μ μ₯ν΄μ νμ©ν  μ μκ³  λ λ€λ₯Έ λ°©λ²μ `this`λ₯Ό λ°μΈλ©νμ§ μλ νμ΄νν¨μλ₯Ό μ¬μ©ν  μ μλ€.
- μ½λ°± ν¨μ λ΄λΆμμμ `this`λ ν΄λΉ μ½λ°± ν¨μμ μ μ΄κΆμ λκ²¨λ°μ ν¨μκ° μ μν λ°μ λ°λ₯΄λ©°, μ μνμ§ μμ κ²½μ°μλ μ μ­κ°μ²΄λ₯Ό μ°Έμ‘°νλ€.
- μμ±μ ν¨μμμμ `this`λ μμ±λ  μΈμ€ν΄μ€λ₯Ό μ°Έμ‘°νλ€.
- λν, λͺμμ μΌλ‘ `this` λ°μΈλ©ν  μ μλλ°, `call`, `apply` λ©μλλ `this`λ₯Ό λͺμμ μΌλ‘ μ§μ νλ©΄μ ν¨μ λλ λ©μλλ₯Ό νΈμΆνλ€. λμ κΈ°λ₯μ μΌλ‘λ μμ ν λμΌνλ μ°¨μ΄μ μ `apply`λ λ°°μ΄λ‘ λ°μ κ·Έ λ°°μ΄ μμλ€μ νΈμΆν  ν¨μμ λ§€κ°λ³μλ‘ μ§μ νλ€.
- ES5μ μΆκ°λ `bind` λ©μλλ `call`κ³Ό λΉμ·νμ§λ§ μ¦μ νΈμΆνμ§ μκ³  λκ²¨λ°μ `this` λ° μΈμλ€μ λ°νμΌλ‘ μλ‘μ΄ ν¨μλ₯Ό λ°ννκΈ°λ§ νλ λ©μλμ΄λ€. κ·Έλ κΈ° λλ¬Έμ `bind` λ©μλλ ν¨μμ `this`λ₯Ό λ―Έλ¦¬ μ μ©νλ κ²κ³Ό λΆλΆ μ μ© ν¨μλ₯Ό κ΅¬ννλ λ κ°μ§ λͺ©μ μ μ§λλ€.
- λν `bind` λ©μλλ₯Ό μ μ©ν΄μ μλ‘ λ§λ  ν¨μλ `name` νλ‘νΌν°μ `bind`μ μλνμΈ `bound` μ λμ΄κ° λΆλλ€. κ·Έλ κΈ° λλ¬Έμ κΈ°μ‘΄μ `call`μ΄λ `apply`λ³΄λ€ μ½λλ₯Ό μΆμ νκΈ°μ λ μμν΄μ§λ€.
- κ·Έλ¦¬κ³  λ©μλμ λ΄λΆν¨μμμ λ©μλμ `this`λ₯Ό κ·Έλλ‘ λ°λΌλ³΄κ² νκΈ° μν λ°©λ²μΌλ‘ `call`, `apply` λλ `bind` λ©μλλ₯Ό μ΄μ©νμ¬ `self`μ κ°μ λ³μλ₯Ό ν μ©νμ§ μμ μ μλ€.
- [this μ λ¦¬ λ΄μ©](https://github.com/saseungmin/reading_books_record_repository/tree/master/%EC%BD%94%EC%96%B4%20%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8/Chapter%203)
## π μμ¨ μΉ΄νκ³ λ¦¬
### π swrμ μ¬μ©ν΄λ³΄κ³  νΉμ§ μ΄μΌκΈ°νκΈ° (axios, fetchμμ μ°¨μ΄μ  λ±...) <μ νμ¬ν­>

### π redux toolkitμ μ¬μ©ν΄λ³΄κ³  νΉμ§ μ΄μΌκΈ°νκΈ°
- λ¦¬λμ€λ₯Ό μ’ λ μ¬μ©νκΈ° νΈλ¦¬νκ² λ§λ€κΈ° μν΄ λ¦¬λμ€μμ κ³΅μμΌλ‘ μ κ³΅νλ κ°λ°λκ΅¬μ΄λ€.
- Redux toolkitμ λ¦¬λμ€μ λ¬Έμ μ μ λ³΄μνκ³ μ λ§λ€μ΄μ‘λλ° λ¦¬λμ€λ₯Ό λΌμ΄λΈλ¬λ¦¬ μμ΄ μ¬μ©ν  μ μ‘μμ μμ±ν΄λ μ‘μ νμμ μ μν΄μΌνκ³  μ‘μν¨μλ₯Ό μμ±νκ³  λ¦¬λμλ₯Ό μ μν΄μΌ νλ λ± λ§μ μμμ΄ νμνλ€. μ΄λ μ΄λ¬ν μ‘μμ κ΄λ¦¬νκΈ° μν΄ λΆλ³μ±μ λ³΄μ‘΄νκΈ° μν immerλ thunk, sagaλ± λ λ€λ₯Έ μλνν° λΌμ΄λΈλ¬λ¦¬κ° μ¬μ©ν΄μΌ νλ€. νμ§λ§ redux toolkitμ λ΄μ₯λ κΈ°λ₯μΌλ‘ sagaλ₯Ό μ μΈν immer produce, λ ν¨ν΄, redux devtools, thunkλ±μ μ§μνκ³  μλ€.
- https://velog.io/@djaxornwkd12/Redux-Toolkit-%EC%95%8C%EC%95%84%EB%B3%B4%EA%B8%B0

### π CORSμ λν΄μ μ€λͺνμΈμ.

#### πΆ CORSλ?
- Cross-Origin Resource Sharing(CORS)μ μΆκ°μ μΈ HTTP headerλ₯Ό μ¬μ©ν΄μ μ νλ¦¬μΌμ΄μμ΄ λ€λ₯Έ originμ λ¦¬μμ€μ μ κ·Όν  μ μλλ‘ ν΄μ£Όλ λ©μ»€λμ¦μ΄λ€. νμ§λ§ λ€λ₯Έ [origin](https://developer.mozilla.org/en-US/docs/Glossary/Origin)μμ λ΄ λ¦¬μμ€μ ν¨λΆλ‘ μ κ·Όνμ§ λͺ»νκ² νκΈ° μν΄ μ¬μ©λλ€.
- μΉ μ νλ¦¬μΌμ΄μμ λ¦¬μμ€κ° μμ μ origin(λλ©μΈ, νλ‘ν μ½, ν¬νΈ)μ λ€λ₯Ό λ Cross-Origin HTTP Request(κ΅μ°¨ μΆμ² HTTP μμ²­)λ₯Ό μ€ννλ€.
- λΈλΌμ°μ λ μ€ν¬λ¦½νΈμμ κ΅μ°¨ μΆμ² HTTP μμ²­μ μ ννλ€. ([XMLHttpRequest](https://developer.mozilla.org/ko/docs/Web/API/XMLHttpRequest)μ [Fetch API](https://developer.mozilla.org/ko/docs/Web/API/Fetch_API)λ [λμΌ μΆμ² μ μ±(same-origin policy)](https://developer.mozilla.org/ko/docs/Web/Security/Same-origin_policy)μ λ°λ₯Έλ€.) μ¦, μ΄ APIλ μ¬μ©νλ μΉ μ νλ¦¬μΌμ΄μμ μμ μ μΆμ²μ λμΌν λ¦¬μμ€λ§ λΆλ¬μ¬ μ μμΌλ©°, **λ€λ₯Έ μΆμ²μ λ¦¬μμ€λ₯Ό λΆλ¬μ€λ©΄ κ·Έ μΆμ²μμ μ¬λ°λ₯Έ CORS ν€λλ₯Ό ν¬ν¨ν μλ΅μ λ°νν΄μΌ νλ€.**
- CORS μ²΄μ λ λΈλΌμ°μ μ μλ² κ°μ μμ ν κ΅μ°¨ μΆμ² μμ²­ λ° λ°μ΄ν° μ μ‘μ μ§μνλ€.
- HTTP μμ²­ ν€λ
  - Origin: cross-site μ κ·Ό μμ²­ λλ preflight requestμ μΆμ²λ₯Ό λνλΈλ€.
  - Access-Control-Request-Method: μ€μ  μμ²­μμ μ΄λ€ HTTP λ©μλλ₯Ό μ¬μ©ν μ§ μλ²μκ² μλ €μ£ΌκΈ° μν΄, preflight request ν  λμ μ¬μ©λλ€.
  - Access-Control-Request-Headers: μ€μ  μμ²­μμ μ΄λ€ HTTP ν€λλ₯Ό μ¬μ©ν μ§ μλ²μκ² μλ €μ£ΌκΈ° μν΄, preflight request ν  λμ μ¬μ©λλ€.

```
OPTIONS /resources/post-here/ HTTP/1.1
Host: bar.other
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.14; rv:71.0) Gecko/20100101 Firefox/71.0
...
Origin: http://foo.example
Access-Control-Request-Method: POST
Access-Control-Request-Headers: X-PINGOTHER, Content-Type
```

- HTTP μλ΅ ν€λ
  - Access-Control-Allow-Origin: λ¨μΌ μΆμ²λ₯Ό γΉμ§μ νμ¬ λΈλΌμ°μ κ° ν΄λΉ μΆμ²κ° λ¦¬μμ€μ μ κ·Όνλλ‘ νμ©νλ€. λλ **μκ²© μ¦λͺμ΄ μλ** κ²½μ° `*` μμΌλ μΉ΄λλ λΈλΌμ°μ μ originμ μκ΄μμ΄ λͺ¨λ  λ¦¬μμ€μ μ κ·Όνλλ‘ νμ©νλ€.
  - Access-Control-Expose-Headers: λΈλΌμ°μ κ° μ κ·Όν  μ μλ ν€λλ₯Ό μλ²μ νμ΄νΈλ¦¬μ€νΈμ μΆκ°ν  μ μλ€.
  - [Access-Control-Max-Age](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Max-Age): preflight request μμ²­ κ²°κ³Όλ₯Ό μΊμν  μ μλ μκ°μ λνλΈλ€.
  - Access-Control-Allow-Credentials: credentials νλκ·Έκ° trueμΌ λ μμ²­μ λν μλ΅μ νμν  μ μλμ§λ₯Ό λνλΈλ€. credentialed request μ μλ΅ν  λ μλ²λ Access-Control-Allow-Origin ν€λ `*` μμΌλμΉ΄λλ₯Ό μ¬μ©νλ λμ μ λ°λμ μ κ°μ μ§μ ν΄μΌ νλ€.
  - Access-Control-Allow-Methods: preflight requestμ λν λν μλ΅μΌλ‘ λ¦¬μμ€μ μ κ·Όν  λ νμ©λλ λ©μλλ₯Ό μ§μ νλ€.
  - Access-Control-Allow-Headers: preflight requestμ λν λν μλ΅μΌλ‘ μ€μ  μμ²­μ μ¬μ©ν  μ μλ HTTP ν€λλ₯Ό λνλΈλ€.

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

#### πΆ CORSκ° μ νμν κΉ?
- λ§μ½ λ΄κ° μλΉμ€νκ³  μμ§ μμ μ¬μ΄νΈμμ μΈμμ μμ²­ν΄μ μΈμμ νλν  μ μλ€λ©΄ ν΄λΉ μ¬μ΄νΈλ μμμ μΌλ‘ λ΄ μΈμμ νμ·¨νκ±°λ λ€λ₯Έ νλμ ν  μ μλ€. κ·Έλμ λΈλΌμ°μ μμλ μ΄λ¬ν μμ²­μ λ§λλ€. νΌμ±μ¬μ΄νΈκ° λνμ μΈ κ³΅κ²© μ¬λ‘μΈλ° μ΄λ¬ν κ²μ λ§κ³  λ΄κ° νμ©ν originλ€λ§ μμ²­ν  μ μλλ‘ νκΈ° μν΄ νμνλ€.

#### πΆ CORSλ μ΄λ»κ² λμν κΉ?
- λΈλΌμ°μ κ° λ¦¬μμ€λ₯Ό μμ²­ν  λ μΆκ°μ μΈ ν€λμ μ λ³΄λ₯Ό λ΄λλ€. λ΄ originμ λ¬΄μμ΄κ³  μ΄λ€ λ©μλλ₯Ό μ¬μ©ν΄μ μμ²­ν  κ²μ΄κ³ , μ΄λ€ ν€λλ€μ ν¬ν¨ν  κ²μΈμ§λ₯Ό λ΄μμ μλ²μ μ μ‘νλ€.
- μλ²λ μλ²κ° μλ΅ν  μ μλ originλ€μ ν€λμ λ΄μμ λΈλΌμ°μ μκ² λ³΄λΈλ€. λΈλΌμ°μ κ° μ΄ ν€λλ₯Ό λ³΄κ³  ν΄λΉ originμμ μμ²­ν  μ μλ€λ©΄ λ¦¬μμ€ μ μ‘μ νμ©νκ³  λ§μ½ λΆκ°λ₯νλ€λ©΄ μλ¬λ₯Ό λ°μμν¨λ€.

#### πΆ Reference
- https://developer.mozilla.org/ko/docs/Web/HTTP/CORS
- https://hannut91.github.io/blogs/infra/cors
