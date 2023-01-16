## 분류 : #jsoup #selectj  

---
## 관련문서
- [[Jsoup]]
- [[Css selectors]]

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

get() 또는 다른 반복문 을 이용해서 element를 구할수있다.
그렇게 Element를 구하고 다음 select를 하는 과정을 반복한다.

혹은 .text() 를 이용해 string을 받거나



----
### 외부문서

----
### 업데이트
-  2022/10/19 (수요일) - 19:16 : 첫 작성
