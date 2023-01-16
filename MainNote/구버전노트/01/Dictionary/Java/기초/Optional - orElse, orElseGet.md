# 제목 : orElse, orElseGet

## 분류 : #optinal #orElse #orElseGet #null

---
## 관련문서
- [[Optional 미완]]
- [[Supplier]]
- 
----
### 요약(사용설명)

---
### 내용

orElse는 null 이던말건 항상불리고
orElseGet은 null 일때만 불린다.

```Java
String username = null;
String result1 = Optional.ofNullable(username)
	.orElse(getDefaultName());
System.out.println(result1); 

String result2 = Optional.ofNullable(username)
	.orElseGet(() -> getDefaultName()); 
System.out.println(result2); }
```

orElse는 값만 취하고 
orElseGet은 "Supplier"를 취한다. 

orElse는 null이여도 함수를 실행 시키고
orElseGet은 null 이면 함수를 실행 시키지 않는다


----
### 외부문서
- [orElse 와 orElseGet의 차이](https://cfdf.tistory.com/34)
- [orElse와 orElseGet의 차이](https://erjuer.tistory.com/102)

----
### 업데이트
-  2022/10/02 (일요일) - 22:07 : 첫 작성







