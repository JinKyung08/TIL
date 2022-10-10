# DAY 04

## -- JAVA --

### ▷반복문

- for문 : 규칙적인 반복, 반복하려는 횟수를 알고 있을 때
-  while문 : 조건이 중요할 때, 조건이 맞지 않으면 한번도 실행하지 않을 수 있음
-  do ~ while문 : 조건이 중요할 때, 반드시 한번은 실행 

**1. for문**
-  for(초기화 ; 조건식(종결식) ; 증감식){
	
	​         조건식이 참인 동안 반복할 문장
	
	}
	
	
	~~~
      public static void main(String[] args) {
	       //ex) 1 ~ 5 까지 합을 구하시오.
   
	        int sum=0;
   
	        for(int i=1; i<=5 ; i++ ) {      // i = i + 1
   
	        sum = sum + i ; // sum += i
   
	        }
   
	        System.out.println("합계 :" + sum);
   
	        }


​	

**2. while**

- 조건이 중요할 때 
		while(조건식){
			조건식이 참일 때 반복할 문장들
		}	
	
	​	ex) while(kor>=60)
	​	    while(true)
	
	~~~
	   public static void main(String[] args) {
	      // 1 ~ 5까지 합을 구하시오.
	      
	      int whileSum = 0 ; //합
	      int i = 1; // 시작값
	      
	      //while(조건식){} 
	      while(i<=5) {
	      		whileSum += i; //whileSum = whileSum +i;
	      		i++; 
	      }
	      System.out.println(whileTotal);
	      }
	~~~
	



**3. do - while** 

~~~
do{

	실행문
    증감식

}while (조건식)
~~~



**4. break**

* 반복문을 빠져나감

- if문의 {}를 제외한 자신과 가장 가까이 있는 {}을 벗어남
- break문 아래쪽 문장은 실행하지 않음

**5. continue**

- 반복문의 조건으로 되돌아 가기
- for문에서는 증감식 부분으로
  while문에서는 조건식 부분으로 올라가기
- continue문 아래쪽 문장들은 실행하지 않음