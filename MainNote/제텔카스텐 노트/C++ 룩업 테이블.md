#룩업테이블 #룩업_테이블 #비교_if_switch
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
	strcpy(tMenu[0].szFoodName, "0번은 라면");
	strcpy(tMenu[1].szFoodName, "1번은 김밥");
	strcpy(tMenu[2].szFoodName, "2번은 순대");

	printf("번호입력: ");
	scanf("%d", &input);
	if(input < 0 || input >2 )
	{
		puts("매뉴없음")
	}
	printf("%s\n", tMenu[iInput].szFoodName);
	return 0;
}
```
이렇게 하는거다

하는 이유는 
선택지를 나열해서 그중 하나를 뽑을때 switch나 if 를쓰는데
if는 우선 조건을 한번씩 비교한다
하지만 switch는 switch의 조건과 case를 모두 한번씩 계산하기 때문에 느리다
하지만 swtich