# DAY 08

## -- Algorithm --

### ▷ 이분검색 (Binary Search)

- 배열에서 데이터가 있는 위치를 찾아주는 검색
- 미리 정렬되어 있는 데이터들을 대상으로 특정한 데이터의 위치를 찾아주는 알고리즘

~~~
ex)
public class BinarySearchExam {
	static int binarySearch (int [] arr, int l, int r, int s) {
		int m =0 ; // 중앙 위치, l은 왼쪽 (시작), r은 오른쪽 (끈) s-찾는값
	
		while(true) {
			// 찾는 값이 없을 때
			if(l>r) {
				return -1;
			}
		
			//찾기, 중간위치 찾기 (시작 + 끝) /2
			m = (l+r)/2;
			if(arr[m] > s) {
				r = m-1;
				continue;
			}else if (arr[m]< s) {
				l = m+1;
				continue;
			}else {
				return m+1; 
			}
	
	
		}	
	}
	public static void main(String[] args) {
	int [] arr = { 14,17,20,22,26,48,50,59,90,100 };
		int result = binarySearch (arr, 0, 9, 20);
		System.out.println(result);
		
		
	}
}
~~~

