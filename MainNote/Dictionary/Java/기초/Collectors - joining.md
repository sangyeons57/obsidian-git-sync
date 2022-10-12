# 제목 : joining

## 분류 : #stream #collectors #list2string #join

---
## 관련문서

----
### 요약(사용설명)

---
### 내용
```Java
list.stream().map(String::valueOf).collect(Collectros.joining(""));
```

python에 join 처럼 나온결과 리스트를 합쳐준다
```Java
Collectors.joining(" ", "{","}");
```
첫번째인수는 element끼리 합칠때 사이에 들어갈 텍스트고
두번째 세번째 는 각각 앞 뒤에 들어갈 텍스트 이다.

다 s


map(String::valueOf)
이부분은 잘 모르겠다

----
### 외부문서
- [관련 내용](https://bactoria.tistory.com/74)

----
### 업데이트
-  2022/10/12 (수요일) - 13:23 : 첫 작성
