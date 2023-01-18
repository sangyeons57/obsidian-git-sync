#전처리기 #룩업테이블 #메클 #define #cpp 

[전처리기 관련 내용](https://www.iar.com/kr/knowledge/learn/programming/basics-of-using-the-preprocessor/)

전처리기는 컴파일 되기 직전에 코드를 복사 붙여넣기 해서 만든 다음 
컴파일 하는 기능

### \# include 지시어
지시어를 찾으면 지정된 파일을 열고 해당내용을 넣으면 파일의 내용이 그위치에 작성된것처럼 컴파일 된다.

### \# Macros
\#define NUM 0
위와 같은 방식으로 사용된다
그러면 NUM이 쓰인곳을 다 0으로 컴파일 되기 전에 바꾼다