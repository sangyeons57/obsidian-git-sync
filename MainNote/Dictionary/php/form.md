## 분류 : #form #post #action

---
## 관련문서

----
### 요약(사용설명)

---
### 내용

```php
  
<form action="파일이름">
    <p> <input type="text" name="title" placeholder="Title"> </p>
    <p> <textarea name="description" placeholder="Description"></textarea> </p>
    <p> <input type="submit"> </p>

</form>

```

submit 타입 인풋을 했을때 파일 읽어오기
name으로 url파라미터 지정
예제)
http:// url ?title="타이틀 인풋" & description="디스크립션 인풋"
이런 식으로 뜸

그런데 이렇게 주소창에 정보가 다나오면 안되는 때가 있는데
이때는
```php
<form action="파일이름" method="POST">
</form>
```
이렇게 하면된다
이 값들을받을때에는
```php
$_get["title"]
이거 대신에
$_post["title"]
이렇게 하면 된다.
```


----
### 외부문서

----
### 업데이트
-  2022/10/30 (일요일) - 19:33 : 첫 작성
