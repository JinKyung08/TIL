# DAY 02

## -- Algorithm --

### ▷ Algorithm

**Basic3**

- 효율성 : 수행 시간 
  - 문제의 크기 : N
- 시간 복잡도 : 주어진 문제를 해결하기 위한 연산 횟수

​				1억 번의 연산을 1초의 시간으로 간주하여 예측

  		1) 빅-오메가 : 최선일 때의 연산 횟수를 나타낸 표기법
  		2) 빅-세타 : 보통일 때의 연산 횟수를 나타낸 표기법
  		3) 빅(Big)-오(O) : O(n) 최악(worst case, 가장 안 좋은)일 때의 연산 횟수를 나타낸 표기법



- StringTokenizer(문자열) ; 

  - 띄어쓰기(한칸 공백을)를 기준을 문자열 구분

- new StringTokenizer(문자열,구분자); 

  - 구분자를 기준으로 문자열 구분

- new StringTokenizer(문자열,구분자, true/false); 

  - 구분자를 기준으로 문자열 구분하되 구분자도 문자열로 처리할 것인가

  - true - 구분자(, ; (...)를 문자열로 처리

  -  false - 구분자는 제외

- hasMoreTokens() : 토큰(구분되어진 문자열)이 있느냐(true반환) 없느냐(false)
- hasMoreElements() : hasMoreTokens()와 같음
- nextToken() : 객체에서 다음 토큰(문자열)을 반환
- countTokens() : 총 토큰의 개수를 반환