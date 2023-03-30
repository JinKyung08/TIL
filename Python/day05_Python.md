# DAY 05

## -- Python --

### ▷ 파이썬 파일 IO

- 파일 생성

~~~
f = open(“test01.txt", 'w')
f.close()
~~~

- 파일 열기 모드
  - r (read) : 읽기모드 - 파일을 읽기만 할 때 사용
  - w (write) : 쓰기모드 - 파일에 내용을 쓸 때 사용
  - a (add) : 추가모드 - 파일의 마지막에 새로운 내용을 추가 시킬 때 사용

- 주요 함수

  - open(“파일명", '열기모드') - 해당 파일명으로 파일 생성
  - close() - 현재 열려있는 파일 객체 종료
  - write( 내용 ) - 파일에 내용을 모두 작성
  - writelines( 내용 ) - 파일에 내용을 작성하되 줄바꿈도 반영
  - read() - 파일의 내용을 전부 문자열로 반환
  - readline() - 파일의 내용을 한 줄씩 문자열로 반환
  - readlines() - 파일의 내용을 한 줄씩 모두 읽어 list로 반환

- with 구문

  - 자바의 try-with-resource와 같이 사용한 뒤 자동으로 close() 수행

  ~~~
  with open('test01.txt', 'r') as file:
  	a = file.read()
  	print(a)
  ~~~

  
