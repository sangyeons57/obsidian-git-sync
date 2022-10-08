# 제목 : count()

## 분류 : #stream #count

---
## 관련문서
- [[Stream()]]
----
### 요약(사용설명)

---
### 내용
```Java
int count = (int) words.stream().filter(w->w.contains("o")).count();
```
typed이 int 가 아니여서(int) 업스케일링? 인가를 해줘야한다.

----
### 외부문서
- [관련설명](https://myhappyman.tistory.com/80)

----
### 업데이트
-  2022/10/08 (토요일) - 17:28 : 첫 작성
