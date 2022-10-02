# 제목 : Supplier T

## 분류 : #함수형 #supplier

---
## 관련문서

----
### 요약(사용설명)

---
### 내용
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

supplier은 불필요한 연산을 필하는 기능이있다
"Lazy Evaluation"
연산을 피하기위해 연산을 지연시키는것


----
### 외부문서
- [supplier](https://m.blog.naver.com/zzang9ha/222087025042)

----
### 업데이트
-  2022/10/02 (일요일) - 22:53 : 첫 작성