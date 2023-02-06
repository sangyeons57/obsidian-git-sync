#cpp  #const #포인터 

```cpp
const int cInt = 10;

int* pInt = (int*)&cInt;

*pInt = 20;
```
cInt는 const여서 문법적으로 변환 할수없지만.
포인터를 이용해서
