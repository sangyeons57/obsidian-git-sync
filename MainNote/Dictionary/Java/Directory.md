## 분류 : #directory #folder #mkdir #deldir 

---
## 관련문서
- [[File]]

----
### 요약(사용설명)

```Java
import Java.io.File;
```
```Java
File f = new File("c:/");

//해당 폴다안에 있는 파일들을 리스트로 반환
String fileList[] = f.list();

```
**listFile() : list()와 유사하지만 String[]을 반환하지 않고 File[]을 반환한다. 따라서 이름만 확인하는게 아니라 각각의 파일에 대해 추가적인 처리를 하고 싶을 때 사용할 수 있다.**  
  
**isFile() : 디렉터리가 아닌 파일인지를 알려준다. 반환값은 boolean**  
**isDirectory() : 디렉터리인지를 알려준다. 반환값은 boolean**  
  
**getName() : 이름을 알려준다. 반환값은 String


**mkdir() : 하나의 디렉터리(폴더)를 생성한다. 동일한 이름이 있으면 생성 실패. 반환값은 boolean. (성공하면 true)

**mkdirs() : 해당 경로를 형성하는 모든 디렉터리를 만든다. 역시 동일한 이름이 있으면 생성 실패.** **반환값은 boolean. (성공하면 true)





---
### 내용

----
### 외부문서
-[설명](https://blog.naver.com/ziharndwjs/221302590265)

----
### 업데이트
-  2022/10/27 (목요일) - 18:07 : 첫 작성
