# DAY 02

## -- Algorithm --

### ▷ Algorithm

**Basic2**

* 마방진 

  ~~~
  public static void main(String[] args) {
  		//마방진
  		//1  2  3  4  5
  		//   6  7  8  9
  		//     10 11 12
  		//        13 14
  		//			 15
  
  		int [][] t = new int [5][5];
  		int num = 1;
  
  		// 요소에 값 넣기
  		//행
  		for (int i = 0; i < t.length; i++) {
  			//열
  			for (int j = i; j < t[i].length; j++) {
  
  				t[i][j]=num;
  				num++;
  
  			}
  		}
  		//요소에 있는 값 출력
  		for (int i = 0; i < t.length; i++) {
  			for (int j = 0; j < t[i].length; j++) {
  				if(t[i][j]==0) {
  					System.out.printf("%2s\t", " ");
  				}else {
  					System.out.printf("%2s\t", t[i][j]);
  				}
  			}
  		System.out.println();
  		}
  		
  	}
  
  ~~~

  

- 2진수 : 0, 1
- 8진수 : 0, 1, 2, 3, 4, 5, 6, 7
- 10진수 : 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
- 16진수 : 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, a, b, c, d, e, f