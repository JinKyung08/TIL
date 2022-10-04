# DAY 11

## --JAVA--

### ▷ Map

- Map 컬렉션은 키(Key)와 값(Value)로 구성된 Entry객체를 저장

- 키는 중복 저장할 수 없지만 값은 중복 저장 가능

- 기존에 저장된 키와 동일한 키로 값을 저장하면 기존의 값은 없어지고 새로운 값으로 대치

- put(key,value) : 주어진 키와 값을 추가, 저장

- containsKey () : 주어진 키가 있는지 여부

- containValue() : 주어진 값이 있는지 여부

- Set<Map.Entry<K,V>> entrySet() : 키와 값의 쌍으로 구성된 모든 Map.Entry 객체를 Set에 담아서 리턴

- get(key) : 주어진 키 값을 리턴

-  Set<K> keySet() : 모든 키를 Set 객체에 담아서 리턴

-  size() : 저장된 키의 총 수를 리턴

-  getKey() : 키에 해당하는 자료 가져오기

-  setValue() : 값에 해당하는 자료 가져오기

  

### ▷ 문자Set

- 경로표시
  - 절대경로 -> ex) c:\ test \ aa.txt
  - 상대경로
    - window : 파일구분 '\\\' 
      -  problem? - System.out.println("\\t,\\n")역슬래쉬를 개행문자로 인식 -> ''\\\\'' 역슬래쉬 2개로 구분 
    - mac : 파일구분 '/'
- ASCⅡ - 특수문자,영문자,소문자,대문자,제어
- 유니코드 - 만국공통어
  - 코드가 안맞으면 깨짐 현상생김
- MS949 - 한글 2byte
- utf-8  - 영,숫,특 - 1byte / 한,중,일 - 3byte



**1. Java.IO (Input Ouput) 입출력**

* 입력 -> 프로그램(컴퓨터) ->출력   / 한방향으로만 감 (Stream)

키보드,마우스,파일,네트워크  -> 프로그램 -> 화면 ,프린트,파일, 네트워크

- 입력 - InputStream (byte단위입력) - reader (문자단위(그림,용량이 높은)) 

- 출력 - OutputStream (byte 단위 출력) - writer (문자단위(그림,용량이 높은))

  ​          -> flush() - 내부버퍼에 잔류하는 바이트를 출혁하고 버퍼를 비움

  						   - 내부 퍼버를 사용하는 이유 : 출력성능을 향상시키기 위해

- 이름.close(); 스트림을 닫아 사용한 메모리를 해제
