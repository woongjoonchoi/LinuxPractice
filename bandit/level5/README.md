file */{.,}*  

\* : 모든 character

\/ :  dicrectory기호 

\*/ : 현재디렉토리  \/  이렇게 나타나거나 , subdriectory  adi/  이렇게 나타난다.  

\*/\* : 현재 디렉토리의 모든파일 /ddd  ,subdriectory  adi/fdf  이렇게 나타난다.  


{.,}  : pattern matching할 때 선택하는 wildcard이다.  . 은 .으로 시작하는 즉, hiddenfile을 나타내고,   , 뒤에 아무것도 없으므로 아무 character도선택하지 않는다.


\*/{.,}*    : */.*  , */* 를 나타낸다. 


!!! \*/* 가 루트디렉토리를 표시하지 않는 이유 : 보안문제 때문이라고 한다. 루트디렉토리를 표시하기 위해서는 명시적으로 \/* 이렇게 적어야 한다.

grep 

결과를 filtering 하는데 사용한다. 

주어진 패턴이 포함된 라인들을 출력

grep -v

주어진 패턴 포함되지 않는  라인들을 출력 

