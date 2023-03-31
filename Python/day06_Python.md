# DAY 06

## -- Python --

### ▷ 파이썬 웹 크롤링

- 웹 크롤링
  - 웹 상에 존재하는 HTML문서, 이미지 등을 주기적으로 수집하여 필요한 데이터만 추출하고 이를 데이터베이스화하는 것으로, 구글, 네이버 등과 같은 검색엔진에서 이를 활용해 링크를 생성해 제공한다.
  - 데이터를 수집하는 방법 중 웹 크롤링은 강력한 수단이 될 수 있지만, 웹 사이트 담당자에게는 서버에 부하를 줄 수 있고 지적 소유물에 대해 **허가를 득하지 않고 가져오는 행위**이기 때문에 검토할 사항들이 많이 존재한다. 따라서 특정 목적으로 웹 크롤링이 필요한 시기가 온다면 반드시 법적 자문을 구하는 것을 권한다.
- robots.txt
  - 웹사이트에서 웹 크롤러같은 로봇들의 접근을 제어하기 위한 규약으로 아직 권고안일 뿐 강제성은 없으나, 2019년을 기준으로 ISO를 포함한 국제 단체들이 의무화를 고려하고 있으며, 사이트에서 크롤링을 원하지 않을 경우 이를 지켜주는 것이 상식이다.

- 크롤링을 위한 외부 모듈 준비
  - requests - HTTP 통신으로 URL을 통한 HTML을 가져올 수 있는 기능을 제공하는 모듈
  - bs4 -  beautifulsoup4, HTTP로부터 받아온 HTML 태그들을 목적에 맞게 파싱하여 필요한 데이터만 추출해주는 모듈
  - selenium - 웹 앱을 테스트하는데 이용하는 프레임워크로, 웹 브라우저를 제어하여 서버에서 전송하는 정보를 모두 수집한다.

- request

  ~~~
  import requests
  
  html = requests.get(‘https://www.google.com’)
  print(html.text)
  ~~~

  

- beautifulsoup4

  - 지정한 HTML을 DOM 형식으로 접근하여 soup.title, soup.title.string 등 으로 접근이 가능케 한다.

  ~~~
  import requests
  from bs4 import BeautifulSoup
  html = requests.get('http://media.daum.net/digital/')
  soup = BeautifulSoup(html.text, 'html.parser')
  print(soup)
  ~~~

  - beautifulsoup4 함수	
    - find / find_all( 태그명[, {속성명: 속성값, . . . }])
      - 해당 태그 명[, 속성값] 을 가진 첫번째 / 모든 태그 추출
    - select / select_one( 선택자 )
      - 특정 선택자에 해당하는 가진 모든 / 첫번째 태그 추출
