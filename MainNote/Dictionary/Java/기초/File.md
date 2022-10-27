## 분류 : #file #fileCreate #fileDelete #fileCheck 

---
## 관련문서
- [[Directory]]

----
### 요약(사용설명)

---
### 내용

```Java
import java.io.File;
```
```Java
File newFile = new File("C:/test.txt");
경로부터 파일 이름까지 다 적어야함

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
**exists(): 파일이 존재하는 지 알려준다. 반환값은 boolean.**  
**canWrite(): 쓸 수 있는 파일인지 알려준다.  반환값은 boolean.**  
**canRead(): 읽을 수 있는 파일인지 알려준다.  반환값은 boolean.**  
**delete(): 파일을 삭제한다.  반환값은 boolean.**

**SetReadOnly() : 파일을 읽기 전용으로 설정  
setWritable(true) : 파일을 쓰기 가능으로 설정


----
### 외부문서
-[설명](https://blog.naver.com/ziharndwjs/221302590265)

----
### 업데이트
-  2022/10/27 (목요일) - 17:59 : 첫 작성
