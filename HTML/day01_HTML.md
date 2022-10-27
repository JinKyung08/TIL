# DAY 01

## -- HTML --

### ▷ HTML (Hyper Text Markup Language)

- 웹페이지를 제작하는 언어

- 웹표준 - html5, css3, Javascript

- 구조(틀) : html

- 꾸밈 : css

- 동적인 부분 : Javascript

  

#### 1. 글자 태그

- <!-- --> :주석

- html의 기본

  ~~~
  <!DOCTYPE html> <!-- html5로 작성한 문서-->
  <html lang="ko">  <!-- html: html태그(요소), lang: 속성, "ko" : 값 -->
    <head>   <!-- 대소문자 구문하지 않음, head태그 : 웹페이지 정보, 스타일시트, 자바스크립트 제목, 외부 링크문서... -->
      <title>웹페이지 제작 연습</title>
      <meta charset="utf-8"> <!-- meta 태그 : 웹페이지에 대한 정보 제공 -->
  
    </head>
    <body> <!-- body 태그 : 일반적으로 웹페이지에 나타나는 부분을 작성-->
  	즐거운 시간<br/><br/> <!-- br : 줄바꿈(자바의 \n과 같은 기능)-->
      HTML 요소&nbsp;&nbsp;&nbsp;&nbsp;연습 <!-- &nbsp; : 한칸공백-->
      <br/>
      <br/> <!-- 줄단위 / 블록단위 복사 : Shift + Alt + 위/아래 방향키 
                 줄단위 / 블록단위 이동 : alt + 위/ 아래 방향키-->
      Copyright &copy; 2022 JK
    </body>
  </html>
  ~~~

  

- \<h1>\</h1> : heading제목
- \<h2>\</h2> 
- \<h3>\</h3> 
- \<h4>\</h4> 
- \<h5>\</h5> 
- \<h6>\</h6> 
- \<hr/>  :수평선 horixontal rule 
- \<p>\</p> : 본문 문단 생성
- \<br/> or \<br> : 줄바꿈
- $nbsp; : 공백
- \&lt; : < 
- \&gt; : >

#### 2. 목록 태그

- \<ol> : 순서가 있는 목록생성

- \<ul> : 순서가 없는 목록 생성

- \<li> : 목록요소 생성

  ```
  ex)
  ul>li*4
  -> <ul>
    	<li></li>
   	<li></li>
    	<li></li>
    	<li></li>
     </ul>
  ```

- 중첩목록

  ~~~
  ex)
  <ul>
    <li>회사소개</li>
    <li>추천도서
     <ul>
        <li>저학년</li>
        <li>중학년</li>
        <li>고학년</li>
      </ul>
    </li>
    <li>프로그램</li>
    <li>열린공간</li>
    <li>동아리</li>
  </ul>
  ~~~

  

- \<div>~\</div> : 블록레벨 태그
- \<span>~\</span> : 인라인레벨 태그 (줄바꿈 X)

#### 3. 하이퍼링크 

- \<a>~\</a> : 하이퍼링크 걸기 - 현재 있는 곳을 벗어나 다른 곳으로 이동 또는 다른 문서를 보여주기 / 인라인레벨 태그 (줄바꿈X)

- href :이동할 경로

- target : _blank - 새로운 창에 문서열기

  ~~~
  ex)
  <a href="https://www.naver.com" target="_blank">네이버</a><br/>
  <a href="./images/flower_small1.jpg">꽃이미지</a><br/>
  <a href="test2.html">test2문서</a><br/>
  ~~~



- \<img src="~~~" /> : 이미지 삽입

- 이미지와 하이퍼링크 연결

  ~~~
  ex)
  <a href="./images/big_Tree01.jpg" target="_blank"><img src="./images/1.jpg" /></a>
  ~~~

  

#### 4. 스타일

- \<style>~~\</style>

- /*  */ - 주석

- color :  색상명;

- margin - 테투리와 다른 태그사이의 테두리 바깥쪽 여백

- border - 테두리

- padding - 테두리와 글자 사이의 테두리 안쪽 여백, 배경색은 padding 영역까지만 적용

- width - 글자를 감싸는 영역의 가로 크기

- height - 글자를 감싸는 영역의 세로 크기

  ~~~
  ex)
  <style>
      /* 주석설명글*/
      h1{ /* h1- 태그 선택자 */
        color: blue; /* 색상명, #0000ff, rgb(0,0,255) */
        border: 1px solid red;
        text-align: center;   /* text-align : 속성, center : 속성에 해당하는 값*/
        background-color: aquamarine;
      }
      .h1style {  /* 클래스명 -> 클래스 선택자*/
        background-color: blueviolet;
      }
      .h1st1{
        color: aqua;
        border: 3px dotted blue;
        text-align: left;
        background-color: bisque;
      }
  </style>
  ~~~

  