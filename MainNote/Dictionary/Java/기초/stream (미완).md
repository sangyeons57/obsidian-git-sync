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


병렬 스트림 생성

`stream` 메서드 대신에 `parallelStream` 메서드를 호출하면 병렬 스트림을 생성할 수 있습니다. 각각의 스레드에서 작업을 처리할 수 있도록 스트림 요소를 여러 **청크(chunk)**로 분할합니다.
```java
List<String> list = List.of("mad", "play", "...");
Stream<String> stream = list.parallelStream();
```


효율적이게 바꾼 기본타입 스트림 int, long, doulbe stream 등이있다.

```java
// 0, 1, 2
IntStream intStream = IntStream.range(0, 3);

// 0, 1, 2, 3
IntStream closedIntStream = IntStream.rangeClosed(0, 3);

// 0, 1, 2
LongStream longStream = LongStream.range(0, 3);

// 0.0, 0.3
DoubleStream doubleStream = DoubleStream.of(0, 3);
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


 

