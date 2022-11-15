# DAY 02

## -- React --

### ▷ 컴포넌트

- 반복적으로 html을 사용할떄 축약하기 위해
- 큰 페이지들 
- 자주 변경되는 것들

- 단점
  - state 가져다 쓸 때 다른 함수(컴포넌트)에 있는 내용이므로 가져다 쓸 수 없음

### ▷ useState

- 형식 -  const[변수명,변수값을 변환할 함수명] = useState(보관할 자료들);

- when to use

  - 변동시 자동으로 html에 반영되게 만들고 싶을때 state를 사용

    변수가 값을 넣었다가 다른 것으로 변경되면 html에 자동으로 변경되지 않기 때문에 따로 변경시켜야 함

    - useState라는 문법을 이용하면 자동으로 html을 재렌더링(반영) 

    - 자주 변경할 html부분은 state로 만들어 사용

- 코드작성

  - 1단계 : import{useState} from 'react';
  - 2단계 : const [변수명,변수값을 변환할 함수명] = useState(보관할 자료들);
  - 3단계 : 함수명에 새롭게 변경할 값을 넣어 주기 

- array, object state 변경하는 방법

  - ex) 예를 들어 let[title,setTitle] = useState(['사과','딸기','바나나']);

    title[0]가 '사과'인데 이것을 '복숭아'로 변경하려면

    - 방벙1) 전체 배열을 바꾼다.

    - 방법2) [0]요소의 값만 변경

      array 자료[0]='바꿀값' =====> setTitle을 title의 값을 넣음

    - 방법3) array, object자료를 원본 데이터를 직접 조작하지 않고

      기존값을 보존하기 위해 복사하고 코드 짬 (가장좋은 방법)

      - let copy = title;

        copy[0]='복숭아';

        setTtitle(copy)

    - 방법4) 방법2와 방법3으로 하면 안됨
      - let copy=[...title]

  - ... 의 의미 : spread operator
    -  array나 object 자료형 왼쪽에 붙일 수 있는데 괄호를 벗겨 주세요 

  

  - state 변경함수를 쓸때 기존 'state === 시규 state'가 같은지 비교

    같으면 state 변경 X

    setTitle(copy) 



### ▷ 생명주기, useEffect

- <컴포넌트 lifecycle(생명주기) 훅>
  - 컴포넌트도 생성되고 업데이트되고 소멸됨
  
- 컴포넌트가 보이기 시작하는 시점 -mount

- 컴포넌트가 바뀌는 것 - update

- 컴포넌트가 필요 없어 제거되는 것 - unmount



- 예전코드
  - class Detail extends React.Component{

​			   componentDidMount(){ //mount될때 실행할 간섭코드 넣기} 

​			   componentDidUpdate(){ //Update될때 실행할 간섭코드 넣기} 

​			   componentWillUnmount(){ //Unmount될때 실행할 간섭코드 넣기} 

​			 }



- ES6이후
  - useEffect(()=>{

 			 mount될 때, update될 때 이곳 코드 실행 함(재랜더링)

 			 console.log("mount될 때 실행"); // 콘솔로 확인

​			})



- useEffect 사용 이유 
  - useEffect안에 있는 코드는 html랜더링 후에 동작
  - useEffect안의 코드들은 시간이 많이 걸리는 어려운 연산
  - 서버에서 데이터 가져오는 작업
  - 타이머 장작하는 코드 들에 주로 사용