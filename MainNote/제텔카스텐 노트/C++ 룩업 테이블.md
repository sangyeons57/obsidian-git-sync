#룩업테이블 #룩업_테이블
룩업 테이블을 이용하는 이유는각 최적화와 가독성에 있다
우선 룩업테이블은 방법 같은 것이다.
사용은
```Cpp
typdef struct tagMenu
{
	char szFoodName[30];
} MENU;

int main()
{
	int input;
	MENU tMenu[3];
	strcpy(tMenu[0].szFoodName, "0번은 라면")
}


```