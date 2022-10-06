# 제목 : Stream().count();

## 분류 : #stream #count

---
## 관련문서

----
### 요약(사용설명)

---
### 내용
```Java
public static void main(String[] args) {
	//count
	List<String> words = Arrays.asList("book", "desk", "keyboard", "mouse", "cup");
	 int count = (int) words.stream().filter(w->w.contains("o")).count();
	 System.out.println("count >" + count); }
```
"o" 가 포함된 stream의 개수를 찾습니다.



----
### 외부문서

----
### 업데이트
-  2022/10/06 (목요일) - 21:02 : 첫 작성
