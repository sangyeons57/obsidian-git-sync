# 제목 : stream()

## 분류 : #java #stream

---
## 관련문서
- [[stream - map (미완)]]
- [[stream - flatmap (미완)]]

----
### 요약(사용설명)

 컬렉션 으로 셍성 (list)
```java
// of 메서드는 자바 9부터 지원
List<String> list = List.of("mad", "play");
Stream<String> stream = list.stream();

```

배열 (array)로 생성
```java
String[] arr = new String[]{"mad", "play"};
Stream<String> stream = Arrays.stream(arr);

// 0번 인덱스만 선택(closed range)
Stream<String> specificStream = Arrays.stream(arr, 0, 1);

// "mad" 출력
specificStream.forEach(System.out::println);
```


---
### 내용
람다(lambda) 를 활용할수 있게 해주는 기술
스레드를 활용하지 않고도 병렬로 일을 진행 시킬수있다.


----
### 외부문서
- [stream 01](https://madplay.github.io/post/introduction-to-java-streams)

----
### 업데이트
-  2022 / 09 / 28( 요일 ) - 14:09 : 첫 작성


 

