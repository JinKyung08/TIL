# DAY 01

## -- Algorithm --

### ▷ Algorithm 

**Basic**

1. 주어진 문제 이해와 분석 -> 무엇을 구할 것인가, 조건, ...	

2. 문제 해결 방안 구상 -> 알고리즘(컴퓨터에게 풀이 방법을 알려주고 풀게 하는 것)

3. 컴퓨터 프로그램 작성 -> 코딩

4. 프로그램 실행 및 검증 -> 디버깅

   

-  1 ~ 10 까지의 자연수의 합

  ~~~
  	public static void main(String[] args) {
  	
  int sum1 = 0, n=1;
  
  //----------------------------방법1
  		while(true) {
  			sum1 += n;
  			n++;
  			if(n>10) {break;}
  			}
  // ------------------------------방법2		
  		do {
  			sum1 +=n;
  			n++;
  		}while (n<=10);
  // ----------------------------	방법3	
  		while (n<=10) {
  			sum1 += n;
  			n++;
  		}
  
  		System.out.println("1~10까지의 합은 : " + sum1);
  //-----------------------------방법4		
  		//for문 
  		
  		int sum =0;
  		
  		for (int i = 1; i <= 10; i++) {
  			sum += i;
  		
  		}
  		System.out.println("1~10까지의 합은 : " + sum);
  	}	
  ~~~

  

* 임의 두 수를 입력 받아서 두 수 사이의 합을 구하기
  		단, 입력한 두 수를 포함한 합

  ~~~
  	public static void main(String[] args) {
  	
  //변수 선언 / 초기화
  		int num1 = 0;
  		int num2 = 0;
  		int sum = 0;
  		
  		//입력받기
  		Scanner scan = new Scanner (System.in);
  		System.out.println("숫자 두 개를 입력하세요");
  		num1 = scan.nextInt();
  		num2 = scan.nextInt();
  		
  		//두 수 의 대소 관계
  		if (num1 <= num2) {
  			for (int i = num1; i <= num2; i++) {
  				sum += i;
  			}			
  		}else {
  			for (int i = num2; i <= num1; i++) {
  				sum += i;
  	      }
  		}
  
  //--------------------------------------------
  	// 다른 방법
  		
  		if(num1 >= num2) {
  			int temp=0;
  			temp = num1;
  			num1 = num2;
  			num2 = temp;
  		}
  		for (int i = num1; i <= num2; i++) {
  			sum += i;
  		}	
  		
  		//출력
  		System.out.println("입력한 두 수 : " + num1 + ", " + num2);
  		System.out.println("두 수를 포함한 합은 : " + sum);
  	}	
  ~~~



- 등차수열 : 각 항에 일정한 수를 더하여 다음 항을 만든 것

  - 다음 등차수열에 대하여 200번째 숫자까지의 합을 구하시오.
    - 2, 8, 14, 20, 26, 32, 38,.... +6

  ~~~
  공차 : 더해지는 일정한 수  // 공차 : 6 
  	public static void main(String[] args) {
      
  		int sum = 0, d=6, f=2, n=1, fn=0;
  		
  		
  		while(n<=200) {
  			fn = f + (n-1) * d;
  			sum += fn;
  			n++;
  			
  		}
  		System.out.println(sum);
  }	
  ~~~

  

- 등비수열 : 각 항에 일정한 수를 곱하여 다음 항을 만드는 것

  - 다음 등비 수열에 대하여 10번째 항까지의 합을 구하시오.
    - 2, 6, 18, 54, 162,...

  ~~~
  공비 : 곱하여지는 수
  // 초항 : 2, 공비 : 3 
  //		n : 항의순서  ,초항을 sum에 담아서 n=2
  	public static void main(String[] args) {
  	
  		int a=2;  // 초항
  		int r=3;	//공비
  		int n=2;	// 합계, 합계에 초항값 담음
  		int sum = a;  // 항의 순서, sum에 초항을 담았기에 2부터 시작
  	
  		
  		while(n<=10) {
  			a *= r; // a=a*r;
  			sum += a; // sum = sum + a;
  			n++;
  		}
  		System.out.println(sum);
  		}
  ~~~

  

* 피보나치 수열 : 첫째 및 둘째 항이 1이며 그 뒤의 모든 항은 바로 앞 두 항의 합인 수열

  - 다음 피보나치 수열에 대하여  50번째 항까지의 합을 구하시오.
    - 1,1,2,3,5,8,13,....

  ~~~
  	public static void main(String[] args) {
  	
  long sum = 0; // 합계누적
  		long prevPrevNum =1 ; // n-2, 첫번째항
  		long prevNum =1 ; // n-1, 두번째항
  		long currentNum =0 ; // n-2 + n-1 -> c  ->첫번째항(전전항) + 두번째항(이전항) -> 다음항
  		int n =2 ; // 항 순서
  
  		sum = prevPrevNum + prevNum; //처음 시작: 첫번째항  + 두번째항
  //-------------------------------------------------방법1		
  		while(n<50) {
  			currentNum = prevPrevNum + prevNum;
  				
  				sum += currentNum;
  				prevPrevNum=prevNum; //전전항을 이전항으로 처리
  				prevNum=currentNum;
  				
  				n++;
  			}
  		System.out.println("while 의 sum : " + sum);
  //-----------------------------------------------------방법2		
  		while(true) {
  			currentNum = prevPrevNum + prevNum;
  			sum += currentNum;
  			prevPrevNum=prevNum; //전전항을 이전항으로 처리
  			prevNum=currentNum;
  			n++;
  			
  			if(n==49) {
  				break;
  			}
  		}
  		System.out.println("while 의 sum : " + sum);
  	}
  ~~~



- 3개의 정숫값 가운데 최댓값 구하기

  ~~~
  	public static void main(String[] args) {
  	
  Scanner Scan = new Scanner(System.in);
  		
  		int fNum=0, sNum=0, lNum=0;
  		int max =0; // 첫번째 인덱스의 값, 기준이 되는 값을 담고 
  		
  		System.out.println("정수 3개를 입력하세요.");
  		fNum=Scan.nextInt();
  		sNum=Scan.nextInt();
  		lNum=Scan.nextInt();
  		
  		max = fNum;
  		
  		if(max<sNum) {
  			max = sNum;
  		}
  		if(max<lNum) {
  			max = lNum;
  		}
  		System.out.println("최댓값은 : " + max);
  	}
  ~~~

  

- 3개의 정숫값 가운데 중앙값 구하기

  ~~~
  public static void main(String[] args) {
  		Scanner Scan = new Scanner(System.in);
  		
  		int a=0, b=0,c=0;
  		int med=0;
  		
  		System.out.println("세정수를 입력해주세요.");
  		a=Scan.nextInt();
  		b=Scan.nextInt();
  		c=Scan.nextInt();
  		
  		if((b>=a && c<=a)||(b<=a && c>=a)) {
  			med = a;
  		}else if ((a>b && c<b)||(a<b && c>b)) {
  			med = b;
  		}else {
  			med = c;
  		}
  			
  		System.out.println(med);
  	}
  ~~~

  

* 구구단

  ~~~
  public static void main(String[] args) {
  		
  		//구구단
  		for (int i = 1; i < 10; i++) {
  			System.out.println(i+"단을 출력합니다.");
  			for (int j = 1; j <10; j++) {
  				System.out.println(i + "x" + j + "=" + i*j);
  			}
  		}
  	}
  ~~~

  

* 배열 선언 방법

  ~~~
  int [] array = new int[5];
  
  		array[0] = 10;
  		array[1] = 20;
  		array[2] = 30;
  		array[3] = 40;
  		array[4] = 50;
  --------------------------------
  		int[] array1 = new int[] {10,20,30,40,50};
  --------------------------------		
  		int[] array2;
  		array2=new int[] {10,20,30,40,50};
  --------------------------------		
  		int[] array3 = {10,20,30,40,50};
  --------------------------------		
  		int[] array4= new int[5];
  ~~~

  