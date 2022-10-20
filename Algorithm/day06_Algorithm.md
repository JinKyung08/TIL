# DAY 06

## -- Algorithm --

### ▷ String Builder

1. String 클래스 

   - 변경할 수 없음 (추가, 삭제, 수정등이 안됨)
   - 추가나 수정이 이루어지면 새로운 객체를 생성 (비효율)

2. 버퍼(buffer)활용 

   - 버퍼의 크기는 변할 수 있으니 언제든 추가, 삭제, 수정이 가능 

   - StringBuilder

     - 일반적으로 사용, StringBuilder 객체는 내부에 문자열을 저장하는 버퍼가 있으며, 그 버퍼의 크기는 변할 수 있음 

     - 기본크기 : 16개의 문자를 저장할 수 있는 버퍼를 생성

     - 객체를 생성한 후 문자열 내용을 변경하면 버퍼의 크기를 자동으로 조정 가능

     - append( ) : 문자열을 버퍼에 추가

     - delete(int start, int end) : 문자열의 일부분을 버퍼에서 제거

     - insert(int offset, String s) : offset 위치에 문자열 s를 삽입

     - replace(int start, int end, String s) : 문자열의 일부분을 문자열 s로 대체 

       

   - StringBuffer

     - 다중 thread 환경에서 안정적

### ▷ 버블 정렬 (Bubble sort) 

- 이웃한 두 데이터를 교환하는 과정들을 거치며 정렬하는 방식 
