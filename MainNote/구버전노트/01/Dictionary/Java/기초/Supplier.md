# 제목 : Supplier T

## 분류 : #함수형 #supplier

---
## 관련문서

----
### 요약(사용설명)

---
### 내용

java 8 부터 나온 기능이다
```Java
import java.util.function.Supplier;
public class SupplierExample {
	public static void main(String[] args) { 
		Supplier<String> helloSupplier = () -> "Hello "; 
		System.out.println(helloSupplier.get() + "World"); 
	} 
}
```
매개변수를 받지않고 단순히 무언가를 반환하는 추상매서드가 있다 (get())

[[Lazy Evaluation]]
은 불필요한 연산은 하지 않는 기능 이 있다
연산을 피하기위해 연산을 지연시키는것


----
### 외부문서
- [supplier](https://m.blog.naver.com/zzang9ha/222087025042)

----
### 업데이트
-  2022/10/02 (일요일) - 22:53 : 첫 작성