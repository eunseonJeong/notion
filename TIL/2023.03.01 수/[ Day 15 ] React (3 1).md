# [ Day 15 ] React (3/1)

# `* Daily Study Planner *`

## To Do List

- [x]  TIL 작성(day)
- [x]  TIL 작성(트러블 슛팅)
- [ ]  TIL 작성(달력기록)
- [x]  팀원 스터디

## Self Study

- [ ]  1일 1커밋 실천

## **Study-groud**

- [ ]  

**export** 중복으로 내보내기 가능
**export default** 하나만 보내기 가능 (inport엔 아무거나 적어도 가능 왜? 보낸 값이 하나니깐~)

예외) export가 많을 때
`import *(전체라는 뜻) as 아무 이름 from './ 폴더명'`
return `<아무 이름.export 함수명>`A`</아무이름.export 함수명>`

## 수  3/1

⏱️ **Study Time ::  17H 00M**

- [ ]  09:00 - 11:00
- [ ]  11:00 - 12:30 구조분해할당 강의 듣기
- [ ]  12:30 - 13:30 점심시간
- [ ]  13:30 - 18:00 todolist 코드 분해
- [ ]  18:00 - 19:00 저녁시간
- [ ]  19:00 - 21:30 todolist 수정 및 리액트 강의
- [ ]  21:30 - 01:00 예상기 매니저님 순회
- [ ]  01:00 - 02:00 TIL 작성

---

## 🗂️ React 숙련 시작!

## 금

- [ ]  

## 토

- [ ]  

## 일

- [ ]  Break time

## 월

- 모던 자바스크립트
    - [x]  연산자
    - [x]  조건문
    - [ ]  반복문
    - [ ]  타입
    - [ ]  함수
    - [ ]  배열메서드
    - [ ]  Number 메서드
    - [ ]  String 메서드
    - [ ]  Math 메서드
    - [ ]  Date 메서드

## 화

- 모던 자바스크립트
    - [x]  map
    - [x]  filter
    - [x]  데이터 타입
    - [x]  실행컨텍스트
    

## 수

- 모던 자바스크립트
    - [x]  this 강의
    - [x]  콜백함수 강의
    - [x]  동기, 비동기 강의
    - [ ]  Promise 강의
    - [ ]  클로저 강의
    

## 목

- 모던 자바스크립트
    - [ ]  동기, 비동기 복습
    - [ ]  Promise 복습
    - [ ]  클로저 복습
    

---

## 🗂️ **Study-plan**  :

코드 프롭스로 도전 (3/1 실)→ 버튼 재활용 가능하게 만들어보기→리액트 생명주기 공부

---

## 🙂  오늘 어땠니?

<aside>
✏️  Props 너 뭔데 이렇게 힘드냐 ㅜㅜ 한 페이지에선 잘 되는데 나누니깐 잘 안된다..

</aside>

---

## 🧳  내일 할 것들

**<28일 예상기 매니저님 순회 내용>**

**form onSubmit** ={ (e) => e.preventDefault()} **form은 새로고침하는 성질이 있어서 preven~로 새로고침을 멈춰줌!

**useReducer** : 상위호환 / settodos를 하는 방법만 다름 !!!
const [todos,dispatch] 라고 명시됨
컴포넌트가 아닌 별도의 공간에서의 사용을 가능하게 해줌.

**useContext (createContext 그룹화 시킴)** : props를 연결해주지 않아도 그룹화가 되어있어서 내려받아서 주는 게 가능함 , 보내고 받고 보내고 받는 props를 안하려고 사용함!

⭐컴포넌트(**재사용성)**
⭐Props ( 가족 컴포넌트 만들고 할아버지 데이터를 손손자가 데이터를 읽을 수 있도록 (=내려보내는 것) 해보기)
⭐State 사용방법

⭐리액트의 생명주기(어떤 구성으로 되어있는지 설명할 수 있어야함!)

⭐ES6 (비구조화할당, 스프레드, 삼항연산자)

## <2월 4째주 키워드>

컴포넌트, props, state(상태는 무엇? useState 를 작성을 하고 값을 자유롭게 바꿀 수 있다. 그리고 그 값을 자유롭게 활용할 수 있다.) 를 이해하자
렌더링과 리렌더링

ES6 문법

리엑트란 무엇인지? 꼭 알고가기

JSX 란 무엇인가

styled-component : 스타일이 있는 태그

**form 과 관련한 태그들-과제**

- **option**
- **select**
- **input**
- **form 태그를 사용하는 방법**
- **form 의 submit 의 기본 이벤트가 무엇인가**

---

## 🤔 문제 상황

- 버튼 재활용 하기
    
    ```jsx
    import React from 'react'
    
    function button(size, backColor) { //버튼이 필요한 속성이 뭘까?
      return (
        <button style ={{
            backgroundColor:"backColor" === 'primary' ? 'green' : 'blue',
            width: size === "large" ? "200px" : size === 'medium' ? "120px" : '60px'
        }}>버튼</button>
      )
    }
    
    export default button
    -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    import React from 'react'
    import Button from './Button'
    
    function App() {
      return (
        <div>App</div>
      )
    }
    
    export default App
    ```
    
- id값 중복이 될 때(**배열 안 ID 값 중 가장 큰 값을 찾아, 그 ID 값보다 +1 한 값을 새로운 객체에 할당**해준다.)
    
    ```jsx
    function addButtonHandler(){
        if(todos.length===0){
          const newtodos={
          id: 1,
          title: name,
          value,
          isDone: false,
        }
        setTodos([...todos, newtodos])
        setName('')
        setValue('')
        }else{
          let max_id = todos[todos.length - 1]
          let num = max_id.id
          let max_num = num+1
          const newtodos={
            id: max_num,
            title: name,
            value,
            isDone: false,
          }
          setTodos([...todos,newtodos])
          setName('')
          setValue('')
          console.log(todos)
    
        }
      };
    ```
    
- 수정 로직 계획
    
    //수정 로직 계획
    
    [ ] 안에서 '완료'라고 누른 Todo를 찾아서, 그거를 새로운 Todo로 변경 -> 날려버리고 -> `{name:'' ,isDone: false} ->{name: '' ,isDone:true}`
    // 인덱스를 알아야 함 -> 왜? 날리고 나서 원래 자리로 넣어줘야 하기 때문에 !!!
    
    **findIndex** 를 사용하여 인덱스를 찾아줌
    **.splice()** 원본 배열을 회손시킴(불변성 유지 x) 복사를 해주고 쓰면 됨 !!배열의 요소를 삭제 또는 변경해줌
    **export** 중복으로 내보내기 가능
    **export default** 하나만 보내기 가능 (inport엔 아무거나 적어도 가능 왜? 보낸 값이 하나니깐~)
    예외) export 많을 때
    import *(전체) as 아무이름 from './ 폴더명'
    
    리덕스: 상태관리 라이브러리
    useReducer:리액트 내장 기능 - 리덕스랑 진짜 비슷
    useContext:리액트 내장 기능 - 3주차
    useEffect - 2주차
    useRef - 3주차 이후