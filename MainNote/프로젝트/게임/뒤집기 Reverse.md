#프로젝트 #게임 
보드게임 REVERSE 를 따라서 만들어보는 게임

게임은 하얀면과 빨간면을 동시에가진 말을 이용해서
자기의 색인 면이 많은 사람이 이기는 게임이다

따라서 자신의 색으로 상대방의 말을 최대한 많이 뒤집어야하는데

말을 뒤집는 방법은 내말이 이미 놔두어진 상태에서 새롭게 둘때 그사이에 있는상대방 말들이 뒤집어진다

처음 세팅은 나와 상대의말을 서로 크로스로 두는것에서 시작한다.

1.우선 게임은 내 과거말 과 현재말 사이의 상대방말을 뒤집는 알고리즘을 만들어야한다
내말이 가운데있다고생각할때 각각 위 아레 오른쪽 왼쪽으로 반복문을쏴서
내 말이 나오면 지금까지 반복문에 들어온에들을 값을 바꿔주는 

2.그리고 클릭할때 상대말과 내말이 번갈아가면서 두는 기능을 만들어야한다

3.기본적으로 게임시작할때 4개블록이 존재하는것을 구현해야해



---
[코드 block Class](https://github.com/sangyeons57/ReverseGame/blob/main/ReverseGame/Assets/Script/Reverse/block.cs)
## block.cs
화면에 보이는 둘수있는 각각의 블럭에 들아갈 스크립트이다

colorDict : 특정상태를 가진 상태가들어올때 해당 색에 맞는 색을 주기위해만든 사전
	void: 아직 클릭이 안된상태
	Red, Blue :자신 색

changesetColorMode : 특정상태가들어오면 자기자신인 블럭을 colorDict에 맞춰서 색을 변환시키는 함수

---
[코드 Reverse Class](https://github.com/sangyeons57/ReverseGame/blob/main/ReverseGame/Assets/Script/Reverse/Reverse.cs)
## Reverse.cs
게임 실행에 전체코드가 들어가있다

### class Piece
한칸이 가져야할 정보들을 가지고있다
각 block과 인스턴스에 1대1 연결이 되어있다.

- Status : enum으로 각piece의 상태를표현하는데 사용

- intaceSetting: piece를 생성한직후 piece에 연결될 block과 인스턴스를 설정하기위해 있는함수 block위치,크기,부모와 block내부설정을 한다

- apply: 자신의status를 block color에 적용

- checkXY: piece를 식별할때 XY값을 이용해 같은지 확인하는 함수

- playerInput: 플레이가 클릭할수있는 부분에 클릭했는지 확인하고 뒤집기를 실행한다 잘못된곳일경우 상태를 원상복구시킨다.

### class PieceList
piece들을 다 가지고있는 함수이고
피스 명령을 내릴때 사용하는 클레스이다

- directoin: 뒤집을수있는 곳을 탐색할때 사용할 8가지 방향정보를 가지고있는 2차원배열이다.

- getPiece: pieceList에서 ceckXY를 활용해 x,y값을 받아 해당조건에 맞는 piece를 찾으면 반환 해준다

- checkAllPieceChanged: 게임이 끝났는지 확인할때 사용하는 함수이다.  blue,red개수를 세는 기능이 포함되어있다.

- setFocus: focus를 설정하고 설정한 PieceList클래스를 돌려준다.

- searchDirection: 자신에게 들어온 direction을 이용해 해당 방향으로 둘수있는지확인한다 
	- false를 반환하는경우는
		- piece가 존재하지 않거나
		- status가 null이거나
		- 자신과 같은 상태(색)을 가진 piece를 만났지만 바로옆에 있는 경우이다.
	- true를 반환하는 경우는
		- 플레이어 상태(색)와 블럭에 상태(색)가 같은경우이다.
		- 값을 반환할수없을때는 재귀함수형태로, 가지고있는 방향만큼에 있는 piece를 가진체로 재귀함수를 실행한다. 

	주어진방향으로 피스를 한칸씩 옴겨가면서 재귀함수를 실행하는 함수이다.

- flipDirectionAction: flipDirection을 8방향으로 실행할수있게 도와주는 함수이다.

- flipDirection: searchDirection을 이용해 해당방향으로 둘수있는지 확인하다음에 둘수있는경우 뒤집기를 실행한다, 플레이어가 둔곳도 상태가 Void가 되지 않게 고정한다

- flip: flip을 직접적으로 실행하는 함수이다. 플레이와 같은 상태은 piece를 만나기 전까지 제귀함수를 이용하여 각piece에 상태를 바꾼다

- changePlayerStatus: 플레이어턴을 바꾼다 그리고 플레이어에 턴이 바뀔때 턴이바뀌었다고 표시한다.

### class counterClass 
Blue,Red의 개수를 새고 승패를 확인하기위해 만든 클래스

### class Reverse
코드를 실행시키는부분

- Start
	piece사이의 거리와 크기를 설정한다
	piece를 생성하여 pieceList를 넣고 instaceSetting을 한다
	기본적으로세팅해야할 가운데 4칸에색을 칠한다
- Update
	space를 누르면 턴을 넘길수있는기능
	승패가 결정되면 그결과를 보여주는 부분
	현재 blue와 red의 개수를 보여주는 부분


[코드 Reverse Class](https://github.com/sangyeons57/ReverseGame/blob/main/ReverseGame/Assets/Script/Reverse/Reverse.cs)
[코드 block Class](https://github.com/sangyeons57/ReverseGame/blob/main/ReverseGame/Assets/Script/Reverse/block.cs)