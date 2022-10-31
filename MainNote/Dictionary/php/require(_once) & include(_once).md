## 분류 : #require #lib  

---
## 관련문서

----
### 요약(사용설명)

---
### 내용
파일 import해서 다른 파일의 코드를 가지고 오는것
require는 해당 부분에 코드를 붙여넣는다.
```php
<body>
	<h1>
	require('lib/print.php')
	<h2>
</body>
```


**require_once**
require 가 내가 가져온 다른 파일에서 내가 가젼은 파일이 있어 겹칠경우에 한번만 부를게 한다.
일반적으로는 이걸 사용하고 중첩해서 사용해야할때 require를 씉다

```php
--- 1.php
<?php
function hello()
{
	echo 'hi';
}
?>

--- 2.php
<?php
require('1.php');
?>


--- 3.php
<?php
require('1.php');
require('2.php');

?>
```
이렇게 되면 php3  에서 php1을 한번 부르고 php2를 통해 php1을 한번더 부른다
이러면 같은 함수를 두번 정의 하게되 에러 생긴다.

require는 이프로세스중에 문제가 생기면 스크립트 실행을 중지 시킨다
require는 hl
l



----
### 외부문서
- [설명](https://www.w3schools.com/php/php_includes.asp)

----
### 업데이트
-  2022/10/31 (월요일) - 18:55 : 첫 작성
