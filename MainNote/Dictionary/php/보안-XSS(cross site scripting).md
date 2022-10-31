## 분류 : #security #internet #hacking #xss #CrossSiteScripting 

---
## 관련문서

----
### 요약(사용설명)

---
### 내용
사용자가 입력할수있는 창에 <script></script>코드를 작성하여
자바스크립트를 사용해 웹사이트에 이상동자을 이르키는 것

해결방법
html에서는 <>가 tag로 인식 되어서 작동되기 때문에
"<>" 를 뜻하는 &lt 와 &gt로 괄호를 바꿔줘야한다

php에서는 이것을
```php
echo htmlsepcialchars('<script>alert("hacked");</script>')
```
htmlsepcialchars를 통해 방어할수있다
이것은 <>들을 자동으로 다 텍스트로 변환해줘서 html이상작동릉 이르키지 않게 한다.

그외로 stricky라는 방법이 있는데 선택한 태그 외의 태그를 전부 삭제하는 것인데 따로공부해야한다.

----
### 외부문서
- [영상](https://www.youtube.com/watch?v=8WV1Ym9BjEQ&list=PLuHgQVnccGMAMMNByX8Bf1BkVrShBhj1I&index=39)

----
### 업데이트
-  2022/10/31 (월요일) - 19:35 : 첫 작성
