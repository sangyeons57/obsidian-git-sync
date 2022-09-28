# 제목 : stream 에서 flatmap 과 map 의 차이

## 분류 : #java #stream

---
## 관련문서
- [[stream (미완)]]
- [[stream - map (미완)]]
- [[stream - flatmap (미완)]]


----
### 요약(사용설명)


---
### 내용

`map` 메서드를 사용하면 단일 스트림 안의 요소를 원하는 특정 형태로 변환할 수 있습니다. 아래 코드로 살펴봅시다.
`flatMap` 메서드는 스트림의 형태가 배열과 같을 때, 모든 원소를 단일 원소 스트림으로 반환할 수 있습니다. 아래 코드로 살펴봅시다. 2차원 배열에서 문자열의 길이가 3 보다 큰 문자열을 출력하는 코드입니다.

`map` 은 단일요소를 리턴하고
`flatmap` 은 스트림을 리턴한다.

`map` 메서드는 스트림의 스트림을 반환하는 반면에 `flatMap` 메서드는 스트림을 반환한다고 보면 된다. 
특히 스트림의 형태가 배열인 경우 또는 입력된 값을 또 다시 스트림의 형태로 반환하고자 할 때는 `flatMap`이 유용하다.

`flatmap` 은 값을 돌려줄때 값을 묶이지 않고 1차원 스트림 으로 펴서 준다 
`map`을 쓰면 collect가 작동 안할때가 있다 2차원 으로 되어있어서
예로
map)
```
["A1"], ["A2"], ["A3"], ["A4"]
```

flatMap)
```
["A1", "A2" , "A3", "A4"]
```

이런 느낌으로 스트림을 반환 해준다.

----
### 외부문서
- [flatmap 과 map 의 차이 01](https://www.baeldung.com/java-difference-map-and-flatmap)
- [flatmpa과 map 의 차이 02](https://madplay.github.io/post/difference-between-map-and-flatmap-methods-in-java)
-  
----
### 업데이트
-  2022/09/28 (수요일) - 15:04 : 첫 작성
-  2022/09/28 (수요일) -  19:58 : 보충작성 스트림 개념 ,내용 설명 "차이 02" 이용
