
## 분류 : #equal #같다 #same #string

---
## 관련문서

----
### 요약(사용설명)

---
### 내용
= = 은 주소값을 비교하고
equals 는 대상의 값 자체르 비교한다
따라서
```Java
String s1 = "abc";
String s2 = "abc";
s1 == s2 //true

String s3 = "abc";
String s4 = new String("abc");
s3 == s4 //false
```

----
### 외부문서
- [설명문서 1](https://coding-factory.tistory.com/536)

----
### 업데이트
-  2022/10/24 (월요일) - 20:57 : 첫 작성
