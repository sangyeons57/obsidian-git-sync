# 제목 : Stream().min() / max()

## 분류 : #stream #min #max #optinal 

---
## 관련문서
- [[Stream()]]

----
### 요약(사용설명)

```Java
Optional < T > min (Comparator < ? super T > comparator) 
```

---
### 내용
```Java
String s = squares.stream().filter(s1 -> values.get(s1).length() > 1)
	.min((x, y) -> values.get(x).length() - values.get(y).length())
	.get();
```
비교하는걸 넣고 optional 을 반환한다
아마도 들어온 스트림이 빈경우를 대비하기 위함이 아닐까

어쨌든 그래서 get()을 해줘야한다 [[opt - of]]

----
### 외부문서

----
### 업데이트
-  2022/10/04 (화요일) - 22:25 : 첫 작성
