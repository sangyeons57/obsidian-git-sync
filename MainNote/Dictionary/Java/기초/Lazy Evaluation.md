# 제목 : Lazy Evaluation

## 분류 : #lazyEvaluation

---
## 관련문서


----
### 요약(사용설명)

---
### 내용
Lazy Evaluation 의 기본은 실제로 필요해질때 연산을 시작한다 이다.
반대에는 Eager Evaluation 이 있다.

```Java
a && b ? true : false;
```
에서  && a 의 연산결과에 따라서 b의 실행여부가 결정되기때문에 Lazy Evaluation 이고 할수있다.

Eager Evaluation
```Java
public void sol()
{
	boolean a = test(1);
	boolean b = test(2);
}

static String 
```

----
### 외부문서
- [관련문서1](https://sabarada.tistory.com/153)


----
### 업데이트
-  2022/10/05 (수요일) - 20:30 : 첫 작성
