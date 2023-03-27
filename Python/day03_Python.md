# DAY 03

## -- Python --

### ▷ 파이썬 제어문

- if – else 조건문

  ~~~
  if 조건식 :
  - 띄어쓰기 -> 내용 작성
  elif 조건식 :
  			내용 작성
  else :
              내용 작성
              
  - 띄어쓰기는 공백문자 2개나 4개,tab을 권장
  
  ex) 
  a = 2
  if a == 1 :
  	print(‘a==1’) # or pass (생략)
  elif a == 2 :
  	print(‘a==2’) # or pass (생략)
  else :
  	print(‘a!=1 & a!=2’)
  ~~~

  

- for 반복문

  ~~~
  for 반복할 변수 in 조건 :
  - 띄어쓰기 -> 내용 작성
  else :
  			내용 작성
  			
  - for문과 while 모두반복 조건에 해당하지 않을 때에 대한 else 를 선언 가능
  
  ex)
  sum = 0
  for i in range(11):
  	sum += i
  print(sum))
  --------------------------------
  list = ["This", "is", "a", "book"]
  for s in list:
  	print(s)
  ~~~

  

- range 내장 함수

  - 특정 횟수의 반복을 수행하며 값을 반환하는 함수

  - range( N )    -    0부터 N -1 까지 반복하여 결과 출력     -      range( 3 ) # 0, 1, 2

    range( M, N )    -    M부터 N -1 까지 반복하여 결과 출력      -     range( 3, 6 ) # 3, 4, 5

    range( L, M, N )   -    L부터 M -1 까지 N씩 간격으로       -        반복하여 결과 출력 range( 3, 7, 2 ) # 3, 5

- while 반복문

  ~~~
  while 조건 :
  - 띄어쓰기 -> 내용 작성
  else :
  			내용 작성
  
  - for문과 while 모두 반복 조건에 해당하지 않을 때에 대한 else 를 선언 가능
  
  ex)
  i = 1
  while i <= 10:
  	print(i)
  	i += 1 			# 파이썬은
  					# i++이 없음
  ~~~

  

- break / continue 분기문

  ~~~
  continue :
  	해당 순번의 반복을
  	continue 밑으로 무시
  break :
  	반복 강제 종료
  	
  - 띄어쓰기는 공백문자 2개나 4개, tab을 권장
  
  ex)
  i = 0
  sum = 0
  while True:
  	i += 1
  	if i == 5:
  		continue
  	if i > 10:
  		break
  	sum += i
  
  print(sum)
  ~~~

  
