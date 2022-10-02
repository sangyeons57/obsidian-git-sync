# 제목 : orElse, orElseGet

## 분류 : #optinal #orElse #orElseGet #null

---
## 관련문서
- [[Optinal 미완]]

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
orElseGet은 "Supplier"

----
### 외부문서
- [orElse 와 orElseGet의 차이](https://cfdf.tistory.com/34)

----
### 업데이트
-  2022/10/02 (일요일) - 22:07 : 첫 작성







