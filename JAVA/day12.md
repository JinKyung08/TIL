# DAY 11

## --JAVA--

### ▷ Thread

- program : 하드디스크에 저장된 파일들의 모임

- process : 프로그램이 메모리에 올려져 실행중인 상태 

- thread  : cpu를 사용하는 최소단위

  - 자바프로그램에서의 쓰레드

    - jvm -> main Thread 생성

      ​			시작시점에서 main thread 1개만 존재

1. Thread 생성 방법

   - 방법 1)  Thread class 상속받아 run() 메서드 재정의

   ~~~
   //Thread class 상속받아 run() 메서드 재정의
   
   class Subtitle extends Thread {
    @Override
    public void run() {
    		Thread 작업 내용
     }
    }
    
    //Thread 객체 생성
    
   Thread sub = new Subtitle();
   or
   Subtitle sub = new Subtitle();
    
    //Thread 실행 - start () 메서드
    
   sub.start()
   ~~~

   

   - 방법 2)  Runnable interface 구현

     ​				run(); 추상메서드 구현

     ​				= > Thread 생성자로 Runnable 객체 전달

   

   ~~~
   // Runnable interface를 구현한 클래스 만들기
   //	추상메서드 run()  구현
   
   class Sub implements Runnable {
   	@Override
   	public void run(){
   		thread 작업내용
   	}
   }
   
   // 객체 생성
   
   Runnable 객체 생성 -> Thread객체 생성 : Thread의 생성자에 Runnable 객체 전달
   
   Runnable s = new Runnable();
   Thread t = new Thread(s);
   
   // 쓰레드를 실행
   	t.start();
   	
   ~~~

   

   

   

   ​             