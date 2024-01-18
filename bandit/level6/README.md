Question:  
The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size   



특정 파일을 찾는 명령어인 find를 사용하면 된다.  

어딘가에 있다고 하였으므로 검색경로는 루트부터 시작한다.  
```
find / type -f
```  
user bandit7, group bandit 6, size 333bytes 의 조건을 적용해준다.  
```
find / -type f -user bandit7 -group bandit6 -size 33c 
```  

이렇게 하면 너무 많은 error들이 출력된다. 이 error들을 전부 dev/null 로 redirect하자.  
```
find / -type f -user bandit7 -group bandit6 -size 33c  2>/dev/null
```