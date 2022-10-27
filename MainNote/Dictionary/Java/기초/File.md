## 분류 : #file #fileCreate #fileDelete #fileCheck 

---
## 관련문서

----
### 요약(사용설명)

---
### 내용

```Java
import java.io.File;
```
```Java
File newFile = new File("C:/test.txt");

// 파일생성
newFile.createNewFile()
try {
	if(newFile.createNewFile()) { 
		System.out.println("newFile.txt 생성 성공");
	} else {
		System.out.println("newFile.txt 생성 실패"); 
	} 
} catch (IOException e) {
	e.printStackTrace(); 
}


```



----
### 외부문서
-[설명](https://blog.naver.com/ziharndwjs/221302590265)

----
### 업데이트
-  2022/10/27 (목요일) - 17:59 : 첫 작성
