## 분류 : #json #read 

---
## 관련문서
-[[file_get_contents]]

----
### 요약(사용설명)

---
### 내용
json file을 배열로 변환하는데 사용한다.
```php
$json = file_get_contents('data.json');
$json_data = json_decode($json, true);

echo $json_data;
```

----
### 외부문서
- [설명](https://www.geeksforgeeks.org/how-to-parse-a-json-file-in-php/)
- [설명2](https://www.php.net/manual/en/function.json-decode.php)

----
### 업데이트
-  2022/11/01 (화요일) - 16:10 : 첫 작성
