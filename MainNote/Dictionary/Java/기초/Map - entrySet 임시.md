# 제목 : map.entrySet()

## 분류 : #map #entrySet

---
## 관련문서

----
### 요약(사용설명)

---
### 내용
```Java
int width = 1 +values.get().entrySet().stream()
			.max((x, y) -> x.getValue().length() - y.getValue().length())
			.get().getValue().length();
```
----
### 외부문서
- [entrySet](https://tychejin.tistory.com/31)
----
### 업데이트
-  2022/09/30 (금요일) - 16:33 : 첫 작성







