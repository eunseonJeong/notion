# [ Day 13 ] React (2/27)

# `* Daily Study Planner *`

## To Do List

- [x]  TIL 작성(day)
- [ ]  TIL 작성(트러블 슛팅)
- [ ]  TIL 작성(달력기록)
- [ ]  팀원 스터디

## Self Study

- [ ]  1일 1커밋 실천

## **Study-groud**

- [ ]  

## 월  2/27

⏱️ **Study Time ::  18H 00M**

- [ ]  09:00 - 10:00 운동
- [ ]  10:00 - 12:00 과제시간
- [ ]  12:00 - 13:00 점심시간
- [ ]  13:00 - 18:30 과제 …
- [ ]  18:30 - 19:30 저녁시간
- [ ]  19:30 - 21:30 과제 …
- [ ]  21:30 - 03:00 강의

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

**25일(금 새벽)** 리액트 입문강의 1-11까지 보기(리액트와 다른 언어들 비교/ 컴포넌트 / Props) → 한번 쑤욱 훑기

**26일(토)**1-12~1-21(State) 까지 보기→ 시간이 된다면.. form 과 관련한 태그들 알아보기

**27일(일)** 실습 다시 풀기→ 1-2랑 1-3 강의 다시 들어보기 →

---

## 🙂  오늘 어땠니?

<aside>
✏️   오늘은 과제만 하다가 끝나버렸네 ㅜㅜ 정말 하루가 짧다.. 내일은 자바스크립트 심화강의랑 오늘 했던 todolist 복습도 해야겠다. 더 강해진 내가 되기를rrrrrr

</aside>

---

## 🧳  내일 할 것들

**<23일 이윤 매니저님 순회 내용>**
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

- todolist 과제 완성
    
    ```jsx
    import React, { useState } from 'react'
    import './App.css'
    
    const App = () => {
      //자바스크립트 문법
      const [todo, setTodo] = useState([
        { id: 1, title: '리액트', text: '강의듣기', isdone: false },
        { id: 2, title: '자바스크립트', text: '할 수 있다', isdone: true },
      ]);
    
      const [title, setTitle] = useState('');
      const [text, setText] = useState('');
    
      //제목 버튼
      const titleHandler = event => {
        setTitle(event.target.value);
      }
    
      //내용 버튼
      const textHandler = event => {
        setText(event.target.value);
      }
    
      //추가 버튼 클릭
      const clickAddButton = () => {
        const newArr = {
          id: todo.length + 1,
          title,
          text,
          isdone: false,
        }
        setTodo([...todo, newArr]);
        setTitle('');
        setText('');
      };
    
      //삭제 버튼 클릭
      const clickRemoveButton = (id) => {
        const removeArr = todo.filter(user => user.id !== id);
        setTodo(removeArr)
      };
    
      const clickCheckButton = (id) => {
        const checkArr = todo.map(item => {
          if (item.id === id) {
            if (item.isdone === false) {
              item.isdone = true;
            } else {
              item.isdone = false;
            }
          }
          return item;
        });
        setTodo([...checkArr]);
      };
    
      // const clickCheckButton = (id) => {
      //   const checkArr = todo.map((item) => {
      //     if (item.id === id) { 
      //       item.isdone = !item.isdone
      //       return ([ ...todo, item]);
      //     } else {
      //       return ([...todo]);
      //     }
      //   })
      //   setTodo([...checkArr]);
      // };
    
      return (
        <>
          <div className='app-reactButton'>
            <div>My Todo List</div>
            <div>React</div>
          </div>
    
          <div className='app-reactButton'>
            <div>
              제목 &nbsp; <input value={title} onChange={titleHandler} /> &nbsp;&nbsp;&nbsp;
              내용 &nbsp; <input value={text} onChange={textHandler} />
            </div>
            <div>
              <button class="button btnPush btnPurple" onClick={clickAddButton}>추가하기</button>
            </div>
          </div>
    
          <h2 className='app-reactButton'>Working..</h2>
          <div className='app-title'>
            {
              todo.map(item => {
                if (item.isdone === false) {
                  return (
                    <div className='app-test' key={item.id}>
                      {item.title} <br /> {item.text}
                      <div className='app-button'>
                        <button class="button btnPush btnPurple" onClick={() => clickRemoveButton(item.id)}> 삭제</button>
                        <button class="button btnPush btnPurple" onClick={() => clickCheckButton(item.id)}> 완료</button>
                      </div>
                    </div>
                  )
                }
              })
            };
          </div>
    
          <h2 className='app-reactButton'>Done!</h2>
          <div className='app-title'>
            {/* 버튼을 누르면 여기로 오게끔 > 완료 true면 여기로 오게끔 !!!조건: isdone === true ? Done으로 : 그대로  */}
            {
              todo.map(item => {
                if (item.isdone === true) {
                  return (
                    <div className='app-test' key={item.id}>
                      {item.title} <br /> {item.text}
                      <div className='app-button'>
                        <button class="button btnPush btnPurple" onClick={() => clickRemoveButton(item.id)}> 삭제</button>
                        <button class="button btnPush btnPurple" onClick={() => clickCheckButton(item.id)}> 취소</button>
                      </div>
                    </div>
                  )
                }
              })
            };
          </div>
        </>
      )
    }
    
    export default App
    
    // //제목 내용을 입력하면 기본 배열에 추가가 되기! (스프레드 문법)
    ```
    
    ```jsx
    
    .btnPurple.btnPush {
      box-shadow: 2px 2px 5px 0px #A74982;
      border: none;
      float: right;
    
    }
    
    .btnFade.btnPurple:hover {
      background: #D65BC1;
    }
    .btnPurple {
      background: #D65BC1;
    }
    button.button {
      display: block;
      position: relative;
      float: left;
      width: 100px;
      padding: 0;
      margin: 0 10px 0 0;
      font-weight: 600;
      text-align: center;
      line-height: 40px;
      color: #FFF;
      border-radius: 5px;
      transition: all 0.2s ;
    }
    
    input {
      width: 250px;
      height: 32px;
      font-size: 15px;
      border: 0;
      border-radius: 15px;
      outline: none;
      padding-left: 10px;
      background-color: rgb(233, 233, 233);
    }
    
    .app-style {
      margin: 50px;
      display: flex;
      /* gap: 12px; */
    }
    
    .app-title{
      color: #D65BC1;
      margin: 50px;
      display:flex;
      width: 100%;
      flex-wrap: wrap;
      justify-content: flex-start;
      align-items: center;
    }
    
    .app-test {
      width: 300px;
      height: 200px;
      display: flex;
      flex-direction: column;
    
      border: 6px solid #D65BC1;
      border-radius: 20px ;
    
      align-items: center;
      justify-content: center;
    }
    .app-button{
      margin: 15px;
    }
    
    .app-reactButton{
      display: flex;
      justify-content: space-between;
      padding: 30px;
      margin: 10px;
      height: 50px;
      font-weight: bold;
    }
    
    .app-remove{
      width: 60px;
      height: 30px;
      display: flex;
    
      border: 2px solid red;
      border-radius: 5px;
    
      text-align: center;
    }
    
    /* //css에서 쓸때는 소문자 , - 신경써주기//
    //js에선 중간 대문자 객체배열!!!// */
    ```
    

어려운 부분 : done으로 옮기는 과정이 힘들었다.. 항해 분들이 도와줘서 끝낼 수 있었던 ㅜ…

```jsx
const clickRemoveButton = (id) => {
    const removeArr = todo.filter(user => user.id !== id);
    setTodo(removeArr)
  };

  const clickCheckButton = (id) => {
    const checkArr = todo.map(item => {
      if (item.id === id) {
        if (item.isdone === false) {
          item.isdone = true;
        } else {
          item.isdone = false;
        }
      }
      return item;
    });
    setTodo([...checkArr]);
  };
```

```jsx
<h2 className='app-reactButton'>Working..</h2>
      <div className='app-title'>
        {
          todo.map(item => {
            if (item.isdone === false) {
              return (
                <div className='app-test' key={item.id}>
                  {item.title} <br /> {item.text}
                  <div className='app-button'>
                    <button class="button btnPush btnPurple" onClick={() => clickRemoveButton(item.id)}> 삭제</button>
                    <button class="button btnPush btnPurple" onClick={() => clickCheckButton(item.id)}> 완료</button>
                  </div>
                </div>
              )
            }
          })
        };
      </div>

      <h2 className='app-reactButton'>Done!</h2>
      <div className='app-title'>
        {/* 버튼을 누르면 여기로 오게끔 > 완료 true면 여기로 오게끔 !!!조건: isdone === true ? Done으로 : 그대로  */}
        {
          todo.map(item => {
            if (item.isdone === true) {
              return (
                <div className='app-test' key={item.id}>
                  {item.title} <br /> {item.text}
                  <div className='app-button'>
                    <button class="button btnPush btnPurple" onClick={() => clickRemoveButton(item.id)}> 삭제</button>
                    <button class="button btnPush btnPurple" onClick={() => clickCheckButton(item.id)}> 취소</button>
                  </div>
                </div>
              )
            }
          })
        };
      </div>
```

나는 true 값으로 ‘done’ 으로 옮겨지고, false 값으로 ‘Working’으로 옮겨진다고 생각했다 ..

if 값으로 true인가 false인가 가려내야 위치가 변동된다 !!! 

css가 버튼이 자꾸 나란히 정렬이 되어서 왜 그럴까? 생각했는데 `**flex-direction: column;` 을 줘야 텍스트랑 나란히 정렬이 된다!!!**  CSS도 부족하다고 느낀 todolist였다.. ㅜㅜ

*근데 왜 삼항연산자는 불가능?*

*filter로 어떻게 하는지 궁금.. > filter로 true값만 빼서 done으로 갈 수 있게끔 하면 되는거 아닌가? > 어떻게? ??????*