# [ Day 16 ] React (3/2)

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

## 목  3/2

⏱️ **Study Time ::  16H 00M**

- [ ]  09:00 - 11:00 todolist 만들기
- [ ]  11:00 - 12:30 구조분해할당 강의 듣기
- [ ]  12:30 - 13:30 점심시간
- [ ]  13:30 - 19:00 todolist 만들기
- [ ]  19:00 - 20:00 저녁시간
- [ ]  20:00 - 21:30 todolist 매니저님 코드리뷰
- [ ]  21:30 - 23:00 전해강 매니저님 순회
- [ ]  23:00 - 01:30 TIL 작성
- [ ]  01:30 - 02:00 생활코딩 강의듣기

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

코드 프롭스로 도전 (3/1 실패)→ 버튼 재활용 가능하게 만들어보기→리액트 생명주기 공부

---

## 🙂  오늘 어땠니?

<aside>
✏️ TODOLIST 지옥이 시작되었따 ! ! ! !1

</aside>

---

## 🧳  내일 할 것들

**<28일 예상기 매니저님 순회 내용>**

**form onSubmit** ={ (e) => e.preventDefault()} **form은 새로고침하는 성질이 있어서 preven~로 새로고침을 멈춰줌!

**useReducer** : 상위호환 / settodos를 하는 방법만 다름 !!!
const [todos,dispatch] 라고 명시됨
컴포넌트가 아닌 별도의 공간에서의 사용을 가능하게 해줌.

**useContext (createContext 그룹화 시킴)** : props를 연결해주지 않아도 그룹화가 되어있어서 내려받아서 주는 게 가능함 , 보내고 받고 보내고 받는 props를 안하려고 사용함!

<**3/3  전해강 매니저님 순회 내용**>

EsLink

에어비앤비 룰
함수, 변수, 태그

**useCallback
useMemo
memo**

리덕스는 미들웨어를 사용할수있다. 불변성을 유지할 수 있다.

form 태그는 엔터를 누르면 버튼이 동작하게끔 설정이 되어있음

변수/함수명 신경쓰기

태그를 용도에 맞게 잘 쓰는 법 !!!

리덕스 - 외부 라이브러리, 전역상태관리

검색엔진(SEO)

리덕스 , 리콜 , 등등 중에 왜 리덕스를 쓰냐?
외부 라이브러리를 선택할 떄의 이유를 생각해보기.
콘텍스트 api와 비교해봤을때 ~비교해서 생각해보기.

원티드 > 온보딩

**form 과 관련한 태그들-과제**

- **option**
- **select**
- **input**
- **form 태그를 사용하는 방법**
- **form 의 submit 의 기본 이벤트가 무엇인가**

---

## 🤔 문제 상황

- 수정 로직 계획 짜기
    
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
    
- 항해 퀴즈 풀기(todolist)
    
    Listtodo 폴더
    
    ![todo.jpg](%5B%20Day%2016%20%5D%20React%20(3%202)%20883adcfaa4894ccd9ff728d051f60c69/todo.jpg)
    
    <추가로 완료 / 삭제 등 버튼 만들면 될듯 >
    
    ```jsx
    import React, { useState } from 'react';
    import './App.css'
    
    const TodoForm = ({ todo, setTodo, buttonChange, buttonAdd }) => {
      return (
        <>
    
          <div className='app-title'>
            <h3>오늘할일</h3>
            <div>
              <input type="text" value={todo} onChange={buttonChange} 
              placeholder="할일을 작성해주세요" required/> &nbsp;
              <button style={{
                  border: '2px solid black' ,
                  borderRadius:'10px',
                  padding:'5px',
              }} onClick={buttonAdd} >기록하기</button>
            </div>
          </div>
        </>
      );
    };
    
    const TodoListItem = ({ item }) => {
      return (
        <>
          <p>{item}</p>
        </>
      );
    };
    
    const TodoList = ({ list }) => {
      let listText = <div>할일이 없어요</div>; // 할일이 없을 때 보여줄 텍스트
      if (list.length > 0) {
        listText = (
          <div className='app-test'>
            {list.map((item, i) => (
              <TodoListItem key={i} item={item} />
            ))}
          </div>
        );
      }
    
      return <>{listText}</>;
    };
    
    const TodoListApp = () => {
      const [todo, setTodo] = useState('');
      const [list, setList] = useState([
        '오전 9시에 기상',
        '항해 출석체크 하기',
        '점심시간 운동하기'
      ]);
    
      const buttonChange = (e) => {
        setTodo(e.target.value);
      };
    
      const buttonAdd = () => {
        if (!todo) return;
        setList([...list, todo]);
        setTodo('');
      };
    
      return (
        <>
          <TodoForm 
          todo={todo} 
          setTodo={setTodo} 
          buttonChange={buttonChange} 
          buttonAdd={buttonAdd} />
          <TodoList list={list} />
        </>
      );
    };
    
    const App = () => {
      return (
        <>
          <TodoListApp />
        </>
      );
    };
    
    export default App;
    ```
    
    css
    
    ```jsx
    input {
      width: 250px;
      height: 32px;
      font-size: 15px;
      border: 0;
      border-radius: 15px;
      outline: none;
      padding-left: 10px;
      background-color: #ffff;
    }
    
    .app-title{
      /* height: 100vh; */
      display:flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
    .app-test {
      width: 600px;
      height: 400px;
      display: flex;
      flex-direction: column;
    
      border: 6px solid black;
      border-radius: 20px ;
    
      align-items: center;
      justify-content: center;
      margin-left: auto;
      margin-right: auto;
      margin-top: 20px;
    }
    ```
    
- todolist 값이 여러 번 출력
    
    ```jsx
    ...
      return (
        <div className='FirstBox'>
          <div className='secondBox'>
            <header>TodoList 📝 </header>
            <div>
              <input value={text} onChange={changeBtnHandle} placeholder="할일을 작성해주세요" /> &nbsp;
              <button onClick={clickBtnHandle} > 클릭해! </button>
            </div>
    
            {/* 들어오는 박스 */}
            <div style={{
              fontSize: "15px",
            }}>
              **{
                todo.map(item => {
                  return (
                    <div key={item.id}>
                        <ul>
                          {todo.map((item, index) => {
                            return (
                              <li key={index} className="list-container">
                                  {/* //조건부 렌더링으로 checked면 가운데 줄을 긋고 아니라면 다시 text만 나오게한다. */}
                                  <p className={`${item.checked ? "checked" : ""}`}>{item.text}</p>
                                <button onClick={() => removeBtnHandle(item.id)}> 삭제 </button> &nbsp;
                                <button> 완료 </button> &nbsp;
                              </li>
                            );
                          })}
                        </ul>
                    </div>**
                  )
    
                })
              }
            </div>
          </div>
    
        </div>
    
      )
    }
    
    export default App
    ```
    
    오류 :  텍스트를 입력하면 값이 중복 출력됨
    
    해결 방법: **`{item.text}` 과 map이 중복해서 들어간 부분을 확인.. 그래서 중복 출력되었구나 !!! ㅜㅜ**
    
- todolist 또 만들기
    - 전체 코드
        
        ```jsx
        import React, { useState } from 'react'
        import './App.css'
        
        const App = () => {
          //id값이 안들어가는 실수를 계속 함..
          const [todo, setTodo] = useState([
            { id: 1, text: '리액트 뿌시기..' }
          ]);
        
          const [text, setText] = useState('');
        
          const [checked,setChecked] = useState(false);
        
          const changeBtnHandle = (e) => {
            setText(e.target.value);
          }
        
        //추가
          const clickBtnHandle = () => {
            const newArr = {
              id: todo.length + 1,
              text,
            }
            setTodo([...todo, newArr])
            setText('');
          }
        //삭제
          const removeBtnHandle = (id) => {
            setTodo(todo => todo.filter(e => e.id !== id));
          }
        
          //밑줄치기
          const checkedBtnHandle = () =>{
            if(checked === false){
              setChecked(true);
            } else {
              setChecked(false);
            }
          }
        
          return (
            <div className='FirstBox'>
              <div className='secondBox'>
                <header className='inputBox'>TodoList 📝 </header>
                <div className='inputBox'>
                  <input value={text} onChange={changeBtnHandle} placeholder="할일을 작성해주세요" /> &nbsp;
                  <button onClick={clickBtnHandle} > 클릭해! </button>
                </div>
        
                {/* 들어오는 박스 */}
                <div style={{
                  fontSize: "15px",
                }}>
                  {
                    <ul>
                      {todo.map((item, index) => {
                        return (
                          <>
                          <li key={index} className="list-container">
                            <div className="list-con">
                              <p className={`${item.checked ? "checked" : ""}`}>{item.text}</p>
                            </div>
                          </li>
                          <button onClick={() => removeBtnHandle(item.id)}>삭제</button>
                          <button>확인</button>
                          </>
                        );
                      })}
                    </ul>
                  }
                </div>
              </div>
        
            </div >
        
          )
        }
        
        export default App
        ```
        
        ```jsx
        body {
          background-color: gainsboro;
        }
        input{
          width: 300px;
        }
        
        .inputBox{
          margin-left: 20px;
        }
        
        .FirstBox {
          width: 512px;
          height: 768px;
        
          background: white;
          border-radius: 16px;
          box-shadow: 0 0 8px 0 rgba(0, 0, 0, 0.04);
        
          word-wrap: break-word;
          overflow: auto;
          /* 스크롤현상 */
        
          margin: 0 auto;
          /* 페이지 중앙에 나타나도록 설정 */
        
          margin-top: 96px;
          margin-bottom: 32px;
          display: flex;
          flex-direction: column;
        }
        
        .secondBox {
          margin: 10px;
          font-size: 36px;
        }
        
        /* .thirdBox{
          border: 5px solid blue;
          border-radius: 30px;
          
          height: 100px;
          width: 300px;
          margin-top: 50px;
          margin-left: auto;
          margin-right: auto;
          text-align: center;
          display: flex;
          align-items: center;
        } */
        
        .checked {
          color: grey;
          text-decoration-line: line-through;
        }
        ```
        
    
    ![todolistt.jpg](%5B%20Day%2016%20%5D%20React%20(3%202)%20883adcfaa4894ccd9ff728d051f60c69/todolistt.jpg)
    
    ![todolistt.jpg2.jpg](%5B%20Day%2016%20%5D%20React%20(3%202)%20883adcfaa4894ccd9ff728d051f60c69/todolistt.jpg2.jpg)
    
    고민한 부분 + 추가로 구현하고 싶은 것들
    
    1. 텍스트 양이 많아져도 흰색 박스 안에 담기게끔 어떻게 하면 좋을까? 
    > 스크롤을 이용하자 > `word-wrap: break-word;` `overflow: auto;` 이 두 개를 CSS에 같이 사용하면 스크롤 완성 !!
    2. 날짜를 넣고 싶은데 프롭스를 나눠서 해야 하나? 한국 시간을 어떻게 받아오면 좋을까? api?인가?
    - 날짜기능 구현
        
        ![화면 캡처 2023-03-02 235007.jpg](%5B%20Day%2016%20%5D%20React%20(3%202)%20883adcfaa4894ccd9ff728d051f60c69/%25ED%2599%2594%25EB%25A9%25B4_%25EC%25BA%25A1%25EC%25B2%2598_2023-03-02_235007.jpg)
        
        ![화면 캡처 2023-03-02 235040.jpg](%5B%20Day%2016%20%5D%20React%20(3%202)%20883adcfaa4894ccd9ff728d051f60c69/%25ED%2599%2594%25EB%25A9%25B4_%25EC%25BA%25A1%25EC%25B2%2598_2023-03-02_235040.jpg)
        
    1. 확인’을 누르면 취소 선이 생기게끔 하고싶다. 삭제와 비슷한 방법일 것 같은뎁..
    2. 수정 기능을 넣어도 좋을 것 같다. ( 다음주에 배우니 도전해봐야지 ..!)
- todolist 최종구현
    
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
              <button style={{fontFamily: 'twaysky'}}  class="button btnPush btnPurple" onClick={clickAddButton}>추가하기</button>
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
                        <button style={{fontFamily: 'twaysky'}}  class="button btnPush btnPurple" onClick={() => clickRemoveButton(item.id)}> 삭제</button>
                        <button style={{fontFamily: 'twaysky'}}  class="button btnPush btnPurple" onClick={() => clickCheckButton(item.id)}> 완료</button>
                      </div>
                    </div>
                  )
                }
              })
            }
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
                        <button style={{fontFamily: 'twaysky'}} class="button btnPush btnPurple" onClick={() => clickRemoveButton(item.id)}> 삭제</button>
                        <button style={{fontFamily: 'twaysky'}}  class="button btnPush btnPurple" onClick={() => clickCheckButton(item.id)}> 취소</button>
                      </div>
                    </div>
                  )
                }
              })
            }
          </div>
        </>
      )
    }
    
    export default App
    
    // //제목 내용을 입력하면 기본 배열에 추가가 되기! (스프레드 문법)
    // //제목 내용을 입력하면 기본 배열에 추가가 되기! (스프레드 문법)
    ```
    
    ```jsx
    body{
      font-family: 'twaysky';
    }
    
    @font-face {
      font-family: 'twaysky';
      src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_tway@1.0/twaysky.woff') format('woff');
      font-weight: normal;
      font-style: normal;
    }
    
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
      gap:10px;
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
    

오늘은 todolist 5번 만들어봤다.

- 삼항 연산자에서 한 값만 true 주고 싶을 때 !!! null값을 주면 된다!!!
    
    ```jsx
    JSX 에서 삼항연산자를 사용하고 싶다면 null을 넣어주면 된다.
    
    a==1 ? true: **null**
    ```
    
    ```jsx
    *같은것
    a===1 ? b : null ;
    a===1 && b
    
    *같은것
    a === 1 ? null : b;
    a===1 || b
    ```