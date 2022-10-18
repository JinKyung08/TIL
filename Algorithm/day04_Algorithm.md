# DAY 04

## -- Algorithm --

### ▷ Stack

- **LIFO(Last in First Out)**

  - 후입선출

  - 마지막에 저장한 데이터를 가장 먼저 꺼냄 
  - push - 저장
  - pop - 추출(맨 위의 객체를 반환, 비었을 때 EmptyStackException 발생 )
  - peek - 확인 (맨 위에 저장된 객체를 반환)
  - top - 스택의 가장 위에 있는 자료 
  - empty - 스택이 비어 있는지 알려줌 
  - size - 스택에 저장되어 있는 자료의 개수
  - 활용 : 수식계산, 수식괄호검사, 워드프로세서의 undo/redo, 웹브라우저의 뒤로/앞으로, 단어 뒤집기
  - 스택은 인덱스 번호 : 1, 2, 3, 4,...



### ▷ Queue

- FIFO(First in First Out)

- 먼저 들어간 데이터가 먼저 나오는 구조 

- 은행의 대기표, 최근사용문서, 인쇄작업 대기목록, 버퍼(buffer)

- <데이터가 없는 경우 예외발생 ,예외처리 기증 미포함 메서드>

  - add() - 지정된 객체를 queue에 추가

  - remove() : queue에서 객체를 꺼내서 반환
  - element() : 삭제 없이 요소를 읽어 온다. 

- <데이터가 없는 경우 기본값 출력 (null), 예외처리기능 포함 메서드>

-  offer() : queue에 객체를 저장, 성공하면 true, 실패하면 false

- poll() : queue에 객체를 꺼내서 반환, 비어있으면 null을 반환

- peek() : 삭제없이 요서를 읽어 온다. queue 가 비어있으면 null 반환