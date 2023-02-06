#cpp  #const #포인터 

### const값을 pointer
```cpp
const int cInt = 10;
int* pInt = (int*)&cInt;
*pInt = 20;
cout << cInt << endl;
```
cInt는 const여서 문법적으로 변환 할수없지만.
포인터를 이용해서 매모리에서 직접 변환할수있다
하지만 print해보면 변환이 안되어있는데 cpu에서 10으로 생각하기때문이다
따라서 volatile을 사용해서 매모를 직접 가져오게해야한다.
```cpp
volatile const int cInt = 10;
int* pInt = (int*)&cInt;
*pInt = 20;
cout << cInt << endl;
```
