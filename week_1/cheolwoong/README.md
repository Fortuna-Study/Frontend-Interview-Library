# π 210329 μ§λ¬Έ

## JavaScript
1. constμ varμ μ°¨μ΄μ μ? (μ€ν μ»¨νμ€νΈ κ΄μ μμλ μ€λͺνκΈ°)
  - `var`μ ES6 μ΄μ λΆν° μ¬μ©, `let`κ³Ό `const`λ ES6λΆν° λ±μ₯
  - `var`μ ν¨μ μ€μ½ν, `let`κ³Ό `const`λ λΈλ‘ μ€μ½ν
  - `var`μ λμΌν μ€μ½ν μμμλ μ¬μ μΈ κ°λ₯
    - μ½λμ κ°λμ±μ΄ λ¨μ΄μ§ μ μκ³ , μλ¬ λ°μμ μμΈμ΄ λλ€.
  - λ°λ©΄, `let`κ³Ό `const`λ λμΌν μ€μ½νμμ κ°μ ν€μλλ‘ κ°μ λ³μλ₯Ό μ¬μ μΈν  μ μλ€.
  - μ€ν μ»¨νμ€νΈλ, JSμμ μ½λκ° μ΄λ»κ² λμνλμ§ κ²°μ νλ νκ²½μ μλ―Ένλ€.
    - μ€ν μ»¨νμ€νΈλΌκ³ λ νκ³ , μ΄λ€ κ³³μμλ νκ²½ λ μ½λλΌκ³  μ§μΉ­νλ€.
    - λ³μ, μΈμ(arguments), this, μ€μ½ν μ²΄μΈλ₯Ό κΈ°μ΅νλ€.
    - JS μ€ν¬λ¦½νΈκ° μ€νλ  λ, μ μ­ μ»¨νμ€νΈκ° μκΈ°κ³  ν¨μκ° μμ±λ  λλ§λ€, ν¨μ μ»¨νμ€νΈκ° μκΈ΄λ€.
  - μ€ν μ»¨νμ€νΈκ° μμ±λλ©΄, λ΄λΆμ λ³μ, ν¨μ μ μΈλ¬Έμ΄ μλ‘ μ¬λΌκ°λ€. (νΈμ΄μ€ν)
  - `var`λ‘ μ μΈν λ³μλ μ½λλ₯Ό λ§λκΈ° μ μ, μμμ λ³μμ μ κ·Όνλ©΄ undefinedμ΄ λμ¨λ€.
  - `let`κ³Ό `const`λ νΈμ΄μ€νλμ§λ§, μ½λλ₯Ό λ§λκΈ° μ μ μμμ λ³μμ μ κ·Όνλ©΄ errorκ° λ°μνλ€. (uninitialized μν) 
  - `let`κ³Ό `const`κ° μ μΈλ μ½λλ₯Ό JSμμ ν΄μνλ©΄, undefined κ°μ΄ ν λΉλκ³  ν΄λΉ λ³μμ κ°μ΄ ν λΉλλ©΄, ν΄λΉ κ°μ΄ λ€μ΄κ°λ€.
  - `let`κ³Ό `const`μ κ²½μ°, νΈμ΄μ€νλ μνλΆν° μ½λλ₯Ό λ§λκΈ° μ κΉμ§μ λ²μλ₯Ό DZ(Dead Zone)μ΄λΌκ³  νλ€. λλ TDZ(Temporary Dead Zone), μΌμμ  μ¬κ° μ§λ
  - πμ°Έκ³ 
  - [λ³μμ μ ν¨λ²μμ ν΄λ‘μ , λͺ¨λ JavaScript νν λ¦¬μΌ](https://ko.javascript.info/closure)
  - [μ€ν μ»¨νμ€νΈ, ZeroCho λΈλ‘κ·Έ](https://www.zerocho.com/category/JavaScript/post/5741d96d094da4986bc950a0)
  - [Execution Context, PoiemaWeb](https://poiemaweb.com/js-execution-context)

2. λκΈ° μ²λ¦¬μ λΉλκΈ° μ²λ¦¬μ μ°¨μ΄μ μ μ€λͺν΄λ³΄μΈμ.
  - πμ°Έκ³ 
  - [λκΈ°μ λΉλκΈ°λ°©μμ μ°¨μ΄μ ](https://blog.metafor.kr/164)
  - [μ΄λ²€νΈ λ£¨νμ λ§€ν¬λ‘,λ§μ΄ν¬λ‘νμ€ν¬](https://ko.javascript.info/event-loop#ref-1165)
3. High Order Function(κ³ μ°¨ ν¨μ)λ λ¬΄μμΈκ°?
  - πμ°Έκ³ 
  - [μλ°μ€ν¬λ¦½νΈ κ³ μ°¨ ν¨μ(Higher-Order Function) μ΄ν΄νκΈ°](https://velog.io/@jakeseo_me/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EA%B0%9C%EB%B0%9C%EC%9E%90%EB%9D%BC%EB%A9%B4-%EC%95%8C%EC%95%84%EC%95%BC-%ED%95%A0-33%EA%B0%80%EC%A7%80-%EA%B0%9C%EB%85%90-22-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EA%B3%A0%EC%B0%A8-%ED%95%A8%EC%88%98Higher-Order-Function-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0)

## Web
1. μΉ λΈλΌμ°μ  urlμ www.naver.com λ₯Ό μλ ₯νμ λ, νλ©΄μ΄ λμ€κΈ°κΉμ§ μΌμ΄λλ μΌμ μ€λͺν΄λΌ.
  - μΉ λΈλΌμ°μ κ° url ν΄μ
    - νλ‘ν μ½, λλ©μΈ, ν¬νΈλ₯Ό ν΄μ
    - μ¬λ°λ₯Έ urlμ΄λ©΄ μμ²­ μμ, μλ κ²½μ° μΉ λΈλΌμ°μ μ κΈ°λ³Έ κ²μμμ§μ κ²μμμ²­
  - HSTS(HTTP Strict Transport Security) λͺ©λ‘ νμΈ
    - HSTSλ μΉ μ¬μ΄νΈκ° HTTPSλ‘ ν΅μ ν΄μΌ νλ€κ³  μλ¦¬λ λ³΄μ κΈ°λ₯
    - ν΄λΉ urlμ΄ λͺ©λ‘μ μ‘΄μ¬νλ©΄(μΊμλμ΄ μλ κ²½μ°) HTTPSλ‘ ν΅μ 
    - HTTPλ‘ μμ²­μ λ³΄λλλΌλ, HTTPSλ‘ λ€μ μμ²­μ λ³΄λ
  - λλ©μΈ μ£Όμμ λ§λ IP μ£Όμλ₯Ό μ°Ύλλ€
    - λλ©μΈ μ£Όμλ μ¬λμ μ΅μν μ£Όμ
    - μ»΄ν¨ν°λ λ€νΈμν¬ ν΅μ μ ν  λ, IP μ£Όμκ° νμνλ€
    - ν΄λΉ λλ©μΈμ IP μ£Όμκ° λΈλΌμ°μ  λλ Local DNSμ μ‘΄μ¬νλ©΄, ν΄λΉ IP μ£Όμλ‘ ν΅μ μ μμνλ€
      - μ‘΄μ¬νμ§ μλ κ²½μ°, DNS μλ²μ IP μ£Όμλ₯Ό μμ²­νλ€.
      - λ¨Όμ  root DNS μλ²μ μμ²­, μλ€λ©΄ μ°¨μμ DNS μλ²μ μμ²­
      - www.naver.comμ κ²½μ°, .com λλ©μΈμ κ΄λ¦¬νλ DNS μλ²μ λ¨Όμ  μμ²­, λͺ» μ°ΎμΌλ©΄ naver.com λλ©μΈμ κ΄λ¦¬νλ DNS μλ²μ μμ²­
      - IP μ£Όμλ₯Ό μ°ΎμΌλ©΄ Local DNSλ ν΄λΉ IP μ£Όμλ₯Ό μΊμ±νκ³  μλ΅
  - IP μ£Όμλ₯Ό μ΄μ©ν΄μ, λΌμ°ν°λ₯Ό ν΅ν΄ www.naver.com μλ²κΉμ§μ κ²½λ‘λ₯Ό νμ
  - λ€νΈμν¬ ν΅μ μ νκΈ° μν΄μ IP μ£Όμμ MAC μ£Όμκ° νμ
    - IP μ£Όμλ λΌλ¦¬ μ£Όμ, MAC μ£Όμλ λ¬Όλ¦¬ μ£Όμ
    - MAC μ£Όμλ κ° λΈλ(μ»΄ν¨ν°)μ λ€νΈμν¬ μΈν°νμ΄μ€λ₯Ό μ§μΉ­νλ€. NIC(Network Interface Card)μ ν λΉλ κ³ μ  μλ³ μ£Όμ λλ κ³ μ  μλ³μ
    - ARP(Address Resolution Protocol)μ ν΅ν΄ μλ²μ MAC μ£Όμλ₯Ό μμλΈλ€.
    - λ΄ μ»΄ν¨ν°μμ naver μλ²κΉμ§ λ€νΈμν¬ ν΅μ μ μ¬λ¬ λΈλλ€μ κ±°μΉκ² λ  κ²μ΄λ€.
    - ARPλ₯Ό ν΅ν΄ κ° λΈλλ€κ³Ό λ€νΈμν¬ ν΅μ νλ©΄μ naver μλ²λ‘ ν¨ν·μ μ λ¬νλ κ²μ΄λ€.
  - HTTP ν΅μ μ νκΈ° μν΄μλ TCP μ»€λ₯μμ΄ λμ΄μΌ νλ€.
    - TCP ν΅μ μ νκΈ° μν΄μλ Socket ν΅μ μ΄ νμνλ©° ν΄λΌμ΄μΈνΈ IPμ ν¬νΈλ²νΈ, μλ²μ IPμ ν¬νΈλ²νΈ μ΄ 4κ°μ§ μ λ³΄λ₯Ό ν΅ν΄ 1:1 λ§€μΉ­μ΄ λλ€.
    - TCPλ 3 handshakingμ ν΅ν΄ μ°κ²°μ΄ κ²°μ λλ€.
      - ν΄λΌμ΄μΈνΈμμ Syn ν¨ν·
      - μλ²μμ Syn + Ack ν¨ν·
      - ν΄λΌμ΄μΈνΈκ° λ€μ Ack ν¨ν·
      - TCP μ°κ²° μλ£
    - HTTPS ν΅μ μ΄λΌλ©΄, TCP μ»€λ₯μ νμ TLS(SSL) handshakingμ΄ μΌμ΄λλ€.   
  - TCP μ»€λ₯μμ΄ μ±κ³΅νλ©΄, κ·Έ μ΄νλ‘ HTTP νΈλμ­μ(μμ²­κ³Ό μλ΅)μ΄ λ°μνλ€.
  - HTTP μμ²­/μλ΅ 
    - HTTP μμ²­ λ©μμ§λ μ²«μ§Έμ€μ HTTP λ©μλ / URL / HTTP λ²μ , λμ§Έμ€μ HTTP ν€λ, μμ§Έμ€μ μν°ν°(λ°μ΄ν°)λ‘ κ΅¬μ± 
    - HTTP μλ΅ λ©μμ§λ μ²«μ§Έμ€μ μνμ½λ / μν λ©μμ§ / HTTP λ²μ , λμ§Έμ€μ HTTP ν€λ, μμ§Έμ€μ μν°ν°(λ°μ΄ν°)λ‘ κ΅¬μ±
    - OSI κ³μΈ΅
      - μμ κ³μΈ΅μμ νμ κ³μΈ΅μΌλ‘ λ°μ΄ν°κ° κ³μΈ΅μ μ§λ  λλ§λ€ μΊ‘μνλκ³ , λ€νΈμν¬λ₯Ό ν΅ν΄ μ λ¬λ  λΈλλ‘ μ΄λ
      - ν΄λΉ λ°μ΄ν°λ₯Ό λ°μ λΈλλ νμ κ³μΈ΅μμ μμ κ³μΈ΅μΌλ‘ λ°μ΄ν°λ₯Ό λμΊ‘μννλ©΄μ μ λ¬
      - HTTP λ©μμ§λ μ νλ¦¬μΌμ΄μ κ³μΈ΅(7κ³μΈ΅)μμ μμ±
      - TCP μΈκ·Έλ¨ΌνΈλ μ μ‘ κ³μΈ΅ (4κ³μΈ΅)μμ λ§λ€μ΄μ§λ©°, ν΄λΌμ΄μΈνΈ ν¬νΈμ μλ² ν¬νΈλ₯Ό ν€λμ ν¬ν¨μν€κ³ , HTTP λ©μμ§λ₯Ό κ°μ§κ³  μλ€.
      - IP λ°μ΄ν°κ·Έλ¨(ν¨ν·)μ λ€νΈμν¬ κ³μΈ΅ (3κ³μΈ΅)μμ λ§λ€μ΄μ§κ³ , ν΄λΌμ΄μΈνΈ IPμ£Όμμ μλ² IPμ£Όμλ₯Ό ν€λμ ν¬ν¨μν€κ³ , TCP μΈκ·Έλ¨ΌνΈλ₯Ό ν¬ν¨
      - λ§ν¬ κ³μΈ΅(2κ³μΈ΅)μμλ MAC μ£Όμλ₯Ό ν€λμ ν¬ν¨μν€κ³ , ν¨ν·μ κ°μ§κ³  μλ€.
      - λ¬Όλ¦¬μ  κ³μΈ΅μ ν΅ν΄ λ€νΈμν¬μ μ μν΄μ ν¨ν·μ μ λ¬
  - πμ°Έκ³ 
    - [λΈλΌμ°μ μ URLμ μλ ₯νμ λ λ°μνλ μΌλ€](https://deveric.tistory.com/97)
    - [μΉ λΈλΌμ°μ μ URLμ μλ ₯νλ©΄ μ΄λ€ μΌμ΄ μΌμ΄λ κΉ?](https://owlgwang.tistory.com/1)
    - κ·Έλ¦ΌμΌλ‘ λ°°μ°λ Http & Network Basic
    
2. νλ μμν¬μ λΌμ΄λΈλ¬λ¦¬μ μ°¨μ΄μ 
  - πμ°Έκ³ 
  - μ¬λ¬ ν¬μ€νμ νμΈνμ§λ§, μλ ν¬μ€νμ΄ μλ μμ±ν κΈμΈ λ―νλ€.
  - [νλ μμν¬μ λΌμ΄λΈλ¬λ¦¬μ μ°¨μ΄μ ](https://webclub.tistory.com/458)
3. ν¬λ‘μ€ λΈλΌμ°μ§ μ΄μμ λμνλ λ°©λ²μ μ€λͺν΄μ£ΌμΈμ.
  - πμ°Έκ³ 
  - [ν¬λ‘μ€ λΈλΌμ°μ§](https://velog.io/@seochanh/00003)

## React
1. useCallbackμ μΈμ  μ¬μ©νλκ°?
2. ν΄λμ€ν μ»΄ν¬λνΈμ ν¨μν μ»΄ν¬λνΈμ μ°¨μ΄λ λ¬΄μμΈκ°?
3. JSXλ?
