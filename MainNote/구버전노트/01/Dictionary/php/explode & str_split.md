## 분류 : #explode #split #str_split #string2array


---
## 관련문서

----
### 요약(사용설명)

---
### 내용
스트링을 array타입으로 변환하는 함수 2개
```php
$p = "p1 p2 p3";
$sp = explode(" ", $p);
// sp = ["p1", "p2", "p3"]
```
explode 는
explod(특정문자열, 배열)
을 이용해서 특정 문자열 기준으로 나눈다

```php
$str = "Hello MrB";
$arr1 = str_split($str);
$arr2 = str_split($str, 3);

/* array1
[
[0] => h
[1] => e
[2] => l
[3] => l
[4] => o
[5] =>  
[6] => M
[7] => r
[8] => B
]
*/

/* array2
[0] => Hel
[1] => lo 
[2] => MrB
*/
```


----
### 외부문서
- [explode](https://www.php.net/manual/en/function.explode.php)
- [str_split](https://www.php.net/manual/en/function.str-split.php)

----
### 업데이트
-  2022/11/01 (화요일) - 16:23 : 첫 작성
