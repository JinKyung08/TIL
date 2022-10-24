# DAY 07

## -- Algorithm --

### ▷ 재귀알고리즘

1. 재귀호출
   - 종료시점 알려주기
   - 재귀호출
   
   ~~~
   ex)
   public class FactoryExam {
   
   	public static void main(String[] args) {
   		int i;
   		Scanner s = new Scanner(System.in);
   		System.out.println("숫자를 입력하시오>>");
   		i =s.nextInt();
   		recursive(i);
   		s.close();
   	}
   		static int recursive(int n) {
   			int i;
   			if(n<1) {		// 종료시점
   				return 2;	
   			}else {			//메서드를 처리할 부분
   				i = (2 * recursive(n-1)) + 1;
   				System.out.println(i);
   				return i;		
   			}
   	}
   
   }
   ~~~
   
   ~~~
   ex)
   public class FactoryExam02 {
   		static int factorial(int n) {
   			if(n>0)	//종료시점을 만들기 위해서 조건을 사용
   				return n * factorial (n-1);
   			else 
   				return 1;		//종료시점
   		}
   				
   	public static void main(String[] args) {
   		Scanner s = new Scanner(System.in);
   		
   		System.out.println("정수를 입력하세요");
   		int x= s.nextInt();
   		
   		System.out.println(x + "의 팩토리얼은 " + factorial(x) + "입니다.");
   	}
   
   }
   ~~~
   
   

### ▷ 트리

- 노드 (node) : O
- 간선 (edge) : ㅡ 
- 루트 (root) : 가장 윗부분에 위치하는 노드
- 리프 (leaf) : 가장 아랫부분에 위치하는 노드

##### 1. 깊이 우선 탐색 (DFS, Depth-First search)

- 방문한 node는 다시 방문하지 않는다.
- LIFO 구조 / 스택



##### 2. 너비 우선 탐색 (BFS, Breadth-First search)

- FIFO 구조 / 큐
- 최단경로(지하철) 찾고자할때 이용 ,최소비용 

