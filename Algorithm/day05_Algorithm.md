# DAY 05

## -- Algorithm --

### ▷ 입출력(I/O) 

- 입력과 출력, 예외 발생 시킨다. 반드시 예외처리가 필요, 
- 입력 : 컴퓨터한테 데이터를 Input
  - 파일 데이터를 읽는다, 키보드에서 데이터를 읽는다, 네트워크상의 데이터를 읽는다.
- 출력 : 컴퓨터가 어떤 것을 Output
  - 파일에 데이터를 쓴다, 모니터에 데이터를 출력한다.(쓴다), 네트워크상에 데이터를 전송한다.(쓴다)
- System.out.println(~~) - 출력
- 입출력 API( Input~, Output~)
  - 바이트스트림 (Byte Stream,1byte 단위) : 일반적으로 입출력 ( 문자, 이미지, 동영상, 소리.. 데이터에 주로 사용)
    - InputStream
    - OutputStream
  - 문자스트림 (character stream, 2byte 단위) : 문자열에 주로 사용, 
    - Reader
    - Writer

##### 1) InputStream

- IntputStream (추상)클래스를 이용해서 객체를 만든다.
- 다른 클래스의 메서드에서 리턴되는 타입 객체를 얻는다. 
- read( ) 메서드 : 데이터 읽기
  -  read( ) - 1byte 단위로 읽기, read(byte[ ]) - Byte[ ] 만큼씩 읽음, 속도가 빠름 
  - close( ) : 입력 스트림 닫기
  - available( ) : 읽을 수 있는 바이트의 개수를 리턴

##### 2) OutputStream

- (추상)클래스를 이용해서 객체를 만든다.

- 다른 클래스의 메서드에서 리턴되는 타입 객체를 얻는다.

- 반드시 예외처리와 close( )를 이용래 외부연결 끝내기 

  - write ( ) : 데이터를 쓰기

  - write (byte[ ]) : byte[ ] 값을 쓰기

  - write(byte[ ], int 위치, int 쓰기 숫자) 

  - close( ) : 자원을 반환

  - flush( ) : 스트림의 버퍼에 있는 모든 내용을 출력 소스에 쓰기

     

##### 3) BufferedInputStream / BufferedOutputStream

- 스트림과 프로그램 간에 데이터를 효율적으로 전송하려고 사용하는 메모리

##### 4) DataInputStream / DataOutputStream

- 문자열 읽고, 쓰기
- byte단위로 문자열을 처리하는 InputStream, OutputStream 을 효율적으로 쓰기 위해 고안된 클래스
- 기본자료형이 다 들어가있음