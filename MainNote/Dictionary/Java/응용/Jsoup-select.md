## 분류 : #jsoup #selectj  

---
## 관련문서
- [[Jsoup]]

----
### 요약(사용설명)

---
### 내용
document 나 element 에서특정 테그 안에 있는 내용 혹은 부분으로 가기위해서 쓰느것

```Java
Document document = Jsoup.connect(url).get();
Elements e1 = document.select("tag.class#id");
```
무조건 Elements를 반환 한다 [[Jsoup-type]]
하나만있어도 이다.

get() 또는 다른 반복문 ㅇ


----
### 외부문서

----
### 업데이트
-  2022/10/19 (수요일) - 19:16 : 첫 작성
