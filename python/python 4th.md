# 10장 계속

## map



## 컬렉션 사본

- 전역에 있는 데이터를 참조형이라고 하며, 그 외의 데이터는 기본형이라고 한다.
- list는 참조형에 해당한다.
- list나 문자열은 크기가 고정되지 않아서 데이터 크기가 변할 수 있다.
- stack는 크기가 고정된다.
- 따라서 참조형 데이터를 사용해서 크기가 변할 때는 그 데이터를 Heap에 저장한다.
- 숫자와 진위판정은 값이 고정되기에 기본형이며, 나머지는 다 참조형으로 이해하면 된다.
- 기본형은 call by value만 넘어가고, 참조형은 call by reference만 넘어간다. C는 예외적으로 두가지 방식 다 넘어갈 수 있다.



# 11장 표준모듈

- 모듈이란 일종의 독립되고 규격화된 부품으로서,  
- ceil(x) : 올림 / floor/(x) : 버림
- 현재 시간을 작업할 때에는 매개변수를 생략해도 된다.
- 함수명에 f가 들어있으면 포맷과 관련된 함수일 가능성이 높다.

# 12장. 예외처리

- 에러가 동시에 나는 경우는 없다.
- 예외처리를 하면 실패하는 경우를 따로 처리할 필요가 없다.
- finally는 예외를 무시하고 블럭이 끝날 때 항상 실행해서 끝낸다.
- 만약 try 명령 내에서 return이 존재하게 되면  try 밖 함수 내에 있는 출력문은 실행되지 않는다.







여러줄 주석 다는 것은 Ctrl+/(한번 더 하면 해제)