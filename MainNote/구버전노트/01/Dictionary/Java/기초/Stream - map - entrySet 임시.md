# 제목 : map.entrySet()

## 분류 : #map #entrySet #stream 

---
## 관련문서

----
### 요약(사용설명)

---
### 내용

map을 반복 가능하게 해준다
아직 잘모르겠다 써본다음에 나머지를 적자
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







