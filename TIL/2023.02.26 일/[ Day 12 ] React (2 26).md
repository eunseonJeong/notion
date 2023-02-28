# [ Day 12 ] React (2/26)

# `* Daily Study Planner *`

## To Do List

- [ ]  TIL 작성(day)
- [ ]  TIL 작성(트러블 슛팅)
- [ ]  TIL 작성(달력기록)
- [ ]  팀원 스터디

## Self Study

- [ ]  1일 1커밋 실천

## **Study-groud**

- [ ]  

## 일  2/26

⏱️ **Study Time ::  05H 00M**

- [ ]  11:00 - 12:30 운동
- [ ]  12:30 - 13:00 점심시간
- [ ]  13:30 - 16:30 과제 시작
- [ ]  16:30 - 18:00 낮잠 zZ
- [ ]  18:00 - 18:30 저녁시간
- [ ]  18:30 - 20:30 과제

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

**23일** 자바 스크립트 심화 강의 듣기 [~~심화 3주차(this)~~->~~심화 4주차(콜백함수)~~->~~유튜브 Promise 강의 3개 듣기~~ ->심화 2주차(실행 컨텍스트) -> 심화 1주차(데이터 타입의 종류 등) -> 동적타이핑(책) -> 배열 메서드->Math 메서드-> 심벌 ->DOM(매니저님 노션)->이벤트 타입 정리(책+강의)

**24일** [https://smallzoodevs-organization.gitbook.io/javascript-study-part01-part05/day-05./1](https://smallzoodevs-organization.gitbook.io/javascript-study-part01-part05/day-05./1). 에서 ~~예제 문제~~와 개념 한번 더 복습하고 올려진 ~~유튜브 강의~~도 봐보기! ( 전날 생활코딩으로 봤으니 더 이해가 될거임!) 

~~map / filter~~ → 배열 메서드 →심벌-→  이벤트 타입 정리(책+강의) →**비구조화 할당 → 함수!! →** 렌더링

**25일(금 새벽)** ~~리액트 입문강의 1-11까지 보기~~(리액트와 다른 언어들 비교/ 컴포넌트 / Props) → 한번 쑤욱 훑기

**26일(토)**~~1-12~1-21(State) 까지 보기~~→ 시간이 된다면.. form 과 관련한 태그들 알아보기

**27일(일)** 실습 다시 풀기→ 1-2랑 1-3 강의 다시 들어보기 →

---

## 🙂  오늘 어땠니?

<aside>
✏️   과제를 진행하는데 내가 state를 제대로 이해하지 못했다는 사실을 깨달았다 ㅜ 강의를 다시 들으러 가야 될 것 같다 ㅎㅎ..

</aside>

---

## 🧳  내일 할 것들

**<23일 이윤 매니저님 순회 내용>**

- 리엑트 시작 - 프로젝트 순서( 어떤 순서로 페이지를 구성해나갈지 생각해서 작성해보기)

<리엑트 세팅>
~~프로젝트 세팅~~
폴더정리

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

- 과제 (미완성)
    
    ```jsx
    import React, { useState } from 'react'
    import './App.css'
    
    const App = () => {
      //자바스크립트 문법
      const [users, setUsers] = useState([
        { id: 1, title: '리액트', text: '강의듣기' },
        { id: 2, title: '자바스크립트', text: '할 수 있다' },
      ])
    
      const [title, setTitle] = useState('');
      const [text, settext] = useState('');
    
      //제목 버튼
      const titleHandler = event => {
        setTitle(event.target.vaule);
      }
    
      //내용 버튼
      const textHandler = event => {
        settext(event.target.vaule);
      }
    
     //추가 버튼 클릭
      const clickAddButton = () => {
        const newArr = {
          id: users.length + 1,
          title,
          text,
        }
        setUsers([...users, newArr]);
      };
    
      //삭제 버튼 클릭
      const clickRemoveButton = (id) => {
        const removeArr = users.filter(user => user.id !==id);
        setUsers(removeArr)
      }
    
      return (
        <>
          <div className='app-reactButton'>
            <div>My Todo List</div>
            <div>React</div>
          </div>
    
          <div className='app-style'>
            제목 <input vaule={title} onChange={titleHandler} />
            내용 <input vaule={text} onChange={textHandler} />
            <button type="text" onClick={clickAddButton}>추가하기</button>
          </div>
    
          <div className='app-title'>
            <h2>Working..</h2>
            <div>
              {
                users.map(item => {
                  return (
                    <div className='app-test' key={item.id}> 
                    {item.title} <br /> {item.text}   
                    <button onClick={()=>clickRemoveButton(item.id)}> 삭제</button>
                     <button>완료</button>
                    </div>
                  )
                })
              }
        
          </div>
        </div>
    
          {/* <div className='app-title'>
            <h2>Done!</h2>
            <div className='app-test'>리액트 공부하기<br /><br />
              리액트 기초를 공부해봅시다.
              <button>삭제</button>
              <button>완료</button>
            </div>
          </div> */}
    
        </>
      )
    }
    
    export default App
    
    // //제목 내용을 입력하면 기본 배열에 추가가 되기! (스프레드 문법)
    //state가 설정이 잘 되었나? 모르게쒀,,
    ```
    
    오류: 추가 버튼을 누르면 title,text가 나와야 되는데 빈칸만 나온다 ㅜㅜ