# DAY 06

## -- JavaScript --

### ▷ jQuery

- 주소 연결 방식 - \<script src="https://code.jquery.com/jquery-3.6.1.js">\</script>
- 다운로드 - \<script src="js/jquery-3.6.1.min.js">\</script>

- window.jQuery = window.$ = jQuery

- $(선택자).메서드(매개변수, 매개변수...)

- jQuery시작 -> 문서 객체의 생성 완료 시점을 잡는 이벤트 연결
  - $(document).ready(function(){   })
- attr() : 문서 객체의 속성 조작
- each()  : 선택한 문서 객체에 반복을 적용
  - $('h1').each(function(index, item){ }) 
- $(선택자 : odd) :홀수 
- $(선택자 : even) :짝수 

- length : 선택된 문서 객체의수 

- get() : 선택한 문서 객체 중 하나를 선택, 일반문서 객체 

- $변수명 : 변수명 앞에 $를 붙여 jquery 변수라는 의미로 사용 

- 글자조작

  - test() : html 태그 내부의 문자를 조작 (비교) 자바스크리트 : textContent

  - html() : html 태그 내부의 문자를 조작, html 태그를 인식, (비교) 자바스크립트 :innerHTML
  - val() : 폼필드(양식 필드)의 값을 조작

- 문서객체.생성(추가)

  - $(a).prependTo(b) : a를 b안쪽 앞에 추가, 해당 요소의 처음에 삽
  - $(a).appendTo(b) : a를 b안쪽 뒤에 추가, 해당 요소의 마지막에 삽입
  - $(a).insertBefore(b) : a를 b 앞에 추가
  - $(a).insertAfter(b) : a를 b뒤에 추가

  

  - $(b).prepend(a) : a를 b처음에 추가

  - $(b).append(a) : a를 b 마지막에 추가

   

- $(선택자).animate(속성,시간,콜백함수);