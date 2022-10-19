## 분류 : #jsoup #document #element #type


---
## 관련문서
- [[Jsoup]]

----
### 요약(사용설명)

---
### 내용
#connect #get
Document: Jsoup가 얻어온 HTML전체 문서
```Java
try {
	Document document = Jsoup.connect(url).get();
} catch (Exception ex) {

}
```

Element: Document의 HTML요소
Elements: Element가 모인 자료형, for while등 반복문 이 가능하다.

Connection: Jsoup의 connect 혹은 설정 메소드들을 이용해 만들어지는 객체, 연결을 하기 위한 정보를 담고 있다.

Response: Jsoup가 URL에 접속해 얻어온 결과. Document와 다르게 status 코드, status 메시지나 charset같은 헤더 메시지와 쿠키등을 가지고 있다

----
### 외부문서

- [관련문서](https://partnerjun.tistory.com/42)

----
### 업데이트
-  2022/10/19 (수요일) - 19:09 : 첫 작성
