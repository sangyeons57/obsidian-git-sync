# 제목 : Collectors.toMap()

## 분류 : #collectors #stream #toMap

---
## 관련문서
- [[stream()]]
 ----
### 요약(사용설명)
```
list.stream().collect(Collectors.toMap(
	key -> key,
	key -> otherlist.stream().filter(value -> value.contains(key)).toList(),
	(prev, next) -> next,
	HashMap::new));

```

Collectors.toMap(key -> key , key -> value, (past , now) -> now, HashMap::new)

첫번째인수 key
두번째인수 value
세번째인수 들어올때 값이 겹칠경우 어떻게 할것인지
네번째인수어떤 map인지
	
---
### 내용

----
### 외부문서
- [collectors - toMap](https://kapentaz.github.io/java/Collectors.toMap%EC%9D%80-NPE-%EC%A3%BC%EC%9D%98%EA%B0%80-%ED%95%84%EC%9A%94%ED%95%98%EB%8B%A4/#)

----
### 업데이트
-  2022/09/29 (목요일) - 21:26 : 첫 작성








