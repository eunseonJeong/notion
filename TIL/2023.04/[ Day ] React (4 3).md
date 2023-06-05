# [ Day ] React (4/3)

# `* Daily Study Planner *`

## To Do List

- [x]  TIL 작성(day)
- [x]  TIL 작성(트러블 슛팅)
- [x]  TIL 작성(달력기록)
- [ ]  팀원 스터디

## Self Study

- [x]  1일 1커밋 실천

## **Study-groud**

- [ ]  

## 월 4/3

⏱️ **Study Time ::  12H 00M**

- [ ]  

---

## 🗂️ React 숙련 시작!

## 금

- [ ]  

## 토

- [ ]  

## 일

- [ ]  관리자 회원가입 연결
- [ ]  일반 회원가입 연결
- [x]  로그인 뼈대 잡기
- [x]  메일 인증 알아보기

## 월

- [ ]  Yup ( 유효성검사 라이브러리) 공부
    - [ ]  이메일
    - [ ]  아이디
    - [ ]  비밀번호
- [x]  관리자 회원가입 연결
- [x]  **오류 체크 !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!**
    - [x]  중복 이메일 오류
    - [x]  중복 회사명 오류
    - [x]  페이지 이동은 되지 않음. 그러나 오류 메세지가 ‘중복된 비밀번호라고 뜸’
    - [x]  중복 이름 오류 ( 동명이인이 있다면 회사측에서 조치해야 함. 우리측에서 할 건 없음 왜냐면 회사측에서 홍길동1 / 홍길동2로 구분하던가 그건 회사가 알아서 할 문제..)
    - [x]  비밀번호 확인
- [x]  일반 회원가입 연결
- [x]  pm8시 이후 ~ api명세서 수정사항 반영

## 화

- [x]  로그인 연결
- [ ]  이메일 인증체크
- [ ]  마이다스 역검
- [ ]  코테 2문제 풀기

## 수

- [x]  Yup ( 유효성검사 정규식 라이브러리) 공부
    - [x]  이메일
    - [x]  아이디
    - [x]  비밀번호
- [ ]  이메일 인증 체크
- [ ]  회원가입 시 이름은 중복 체크 안되어있음! 어떻게 하면 좋을지 생각해보기

## 목

- [ ]  이메일 인증 체크

---

## 🗂️ **Study-plan**  :

### <최종 프로젝트>

1. 회원가입 ( 관리자 ) /users/signup/admin
'회사 관리자'는 메일 인증을 통해 고유 번호(companyName)를 받고 고유 번호를 직원들한테 뿌림 !

~~참고) [https://coding-hwije.tistory.com/6?category=856854](https://coding-hwije.tistory.com/6?category=856854)~~

[~~https://bb-library.tistory.com/106~~](https://bb-library.tistory.com/106)

## [**~~https://kibua20.tistory.com/80](https://kibua20.tistory.com/80)  → step 2부터 ... 이어서 해야해요..............~~**

- **관리자 페이지 오류 check**
- [x]  중복 이메일 오류
- [x]  중복 회사명 오류
- [x]  중복 이름 오류 ( 동명이인이 있다면 회사측에서 조치해야 함. 우리측에서 할 건 없음 왜냐면 회사측에서 홍길동1 / 홍길동2로 구분하던가 그건 회사가 알아서 할 문제..)
- [x]  비밀번호 확인
- [ ]  유효성 검사 yup이라는 라이브러리 통해 정규식 간단하게 사용해보기

[react에서 회원가입 form입력받기 (react-hook-form + yup)](https://jisoo-log.tistory.com/17)

1. 회원가입 ( 사원 ) /users/signup/user
고유 번호(companyName) 입력란이 있어야 함
2. 로그인 (관리자&사원) /users/login
가입 시 사용한 이메일, 패스워드 입력하면 됨

- ~~input 컴포넌트로 빼기 ok~~ (일단 로그인& 회원가입 + 마이페이지 ? 부분에서만 사용됨)

---

## 🙂  오늘 어땠니?

<aside>
✏️

</aside>

---

## 🧳  내일 할 것들

- [ ]  

---

## 🤔 문제 상황

- 트러블 슈팅
    
    input 값을 입력 후 ‘확인’ 버튼을 눌렀을 때 빈 값 처리를 해줬는데 왜 빈 값이 안나오는가..
    
    ```jsx
    const sumbitHandler = async (e) => {
        e.preventDefault();
        try{
          if(admin.password === admin.passwordCheck) {
            console.log("유저 !!!",admin);
            await instance.post('/user/signup/admin',admin)
            navi('/login');
            // 인풋값 비우기 왜 안되니????
            setAdmin('');
          }
        }
        catch (e) {
          alert('비밀번호가 일치하지 않습니다.')
        }
      };
    ```
    
    상황: input값이 화면에서 싹 ~ 지워져야하는데 그대로 남아있음..
    
     `setAdmin('');` 을 해주면 되는거아니냐고 !!! 
    
    내가 생각해 본 부분: 내가 form 태그에 해주면 안되는데 위치가 잘못된걸까? 확인 버튼에 저 부분을 넣어줘야 했던걸까? sumbit 함수는 확.인 용이니깐 맞는 로직이 아닌가?! 물론 navi가 들어가 있어 두 개의 역할을 수행하긴 한다 그럼 함수의 이름도 sumbit이 아니라 다른걸로 바꿔줘야 했을까?  아니 .. 일단 값이 안 비워지는건 인풋창의 문제인데 인풋창의 상태는 setAdmin으로 한번에 관리가 되어있어서 활용하면 되는건 맞다!!! 그럼 위치를 바꿔줘보자!!!
    
    결과: 
    
- 트러블 슈팅
    
    (위와 같은 코드임)
    
    ```jsx
    const sumbitHandler = async (e) => {
        e.preventDefault();
        try{
          if(admin.password === admin.passwordCheck) {
            console.log("유저 !!!",admin);
            await instance.post('/user/signup/admin',admin)
            navi('/login');
            // 인풋값 비우기 왜 안되니????
            setAdmin('');
          }
        }
        catch (e) {
          alert('비밀번호가 일치하지 않습니다.')
        }
      };
    ```
    
    상황: 비밀번호를 동일하게 입력했는데 자꾸 ‘비밀번호가 일치하지 않는다’고 뜸
    
    그리고 Priview 부분에서 `msg: "Token Error” statusCode: 401` 라고 뜸.. 토큰의 문제????ㅜ
    
    내가 생각해 본 부분: password와 passwordCheck가 value에 잘 담겨있는지 확인해줬고 admin이 맞는지.. 조건을 다시 한번 확인했다.
    
    결과: 서버 문제였다……..ㅋ..
    

*스키마(Schema): 데이터의 구조와 제약 조건(Validation)을 정의하는 개념입니다. 데이터를 저장하거나 전송하기 위해서는 데이터의 형태, 구성, 제약조건 등을 사전에 정의해야 하며, 이러한 내용을 스키마로 정의합니다.

- 오늘의 고민 (정규식 라이브러리 중 어떤 것을 사용할까?)
    
    정규식 라이브러리 중 어떤 것을 사용할까?
    
    <종류>
    
    - **Formik**
    장점
        - 폼의 상태 관리를 쉽게 할 수 있습니다. Formik은 React의 상태 관리 기능인 useState, useEffect, useContext 등을 활용하여 폼의 상태를 관리합니다. 이를 통해 폼의 값을 쉽게 읽고 변경할 수 있습니다.
        - 유효성 검사 기능을 제공합니다. Yup과 함께 사용하면, Formik은 폼 데이터의 유효성을 검사할 수 있습니다. Yup이 제공하는 다양한 검사 조건을 활용하여, 사용자 입력값의 유효성을 쉽게 확인할 수 있습니다.
        - 다양한 이벤트 처리 기능을 제공합니다. Formik은 onBlur, onFocus, onSubmit 등 다양한 이벤트 처리 기능을 제공합니다. 이를 통해 사용자 입력값의 변화에 따라 적절한 이벤트를 처리할 수 있습니다.
        - 다른 라이브러리와 함께 사용하기 쉽습니다. Formik은 다른 라이브러리와 함께 사용하기 쉽습니다. 예를 들어, Yup, React-Bootstrap, Material UI 등의 라이브러리와 함께 사용할 수 있습니다.
        
        단점
        
        - 일부 기능이 Redux와 비슷하게 동작합니다. Formik은 Redux와 비슷한 방식으로 폼의 상태를 관리합니다. 따라서 Redux를 사용하는 경우, Formik과 충돌이 발생할 수 있습니다.
        
        참고링크
        
        [라이브러리 뽀개기 - Formik](https://velog.io/@seeh_h/라이브러리-뽀개기-Formik)
        
    - **Yup** ( 헷갈려서 적어둠→JavaScript와 TypeScript 모두에서 사용 가능 , JavaScript로 작성된 객체 스키마 검증 라이브러리 )
        
        장점
        
        - 브라우저와 Node.js에서 모두 사용할 수 있습니다. Yup은 브라우저와 Node.js에서 모두 사용할 수 있습니다. 따라서, 서버 측과 클라이언트 측에서 모두 데이터 유효성 검사를 쉽게 할 수 있습니다.
        - 다양한 유효성 검사 규칙을 지원합니다. Yup은 다양한 유효성 검사 규칙을 지원합니다. 예를 들어, required(), min(), max(), email() 등의 규칙을 지원합니다. 이를 통해, 다양한 데이터 유효성 검사를 쉽게 할 수 있습니다.
        - Yup 스키마를 재사용할 수 있습니다. Yup은 스키마를 재사용할 수 있는 기능을 제공합니다. 이를 통해, 다양한 데이터 유효성 검사에서 같은 스키마를 반복해서 사용할 수 있습니다.
        
        단점
        
        - 정규식을 사용하는 경우, 작성이 어렵습니다. Yup은 정규식을 사용하여 유효성 검사를 할 수 있지만, 정규식을 작성하는 것이 어려울 수 있습니다.
        
        참고링크
        
        [react에서 회원가입 form입력받기 (react-hook-form + yup)](https://jisoo-log.tistory.com/17)
        
        [https://github.com/jquense/yup](https://github.com/jquense/yup)
        
        예시
        
        ```jsx
        import { createAction } from "@reduxjs/toolkit";
        import * as Yup from "yup";
        
        export const updateUser = createAction("user/update");
        
        export const updateUserAction = (formData) => async (dispatch) => {
          const schema = Yup.object().shape({
            name: Yup.string().required(),
            age: Yup.number().positive().integer().required(),
            email: Yup.string().email().required(),
          });
        
          try {
            await schema.validate(formData);
            // 폼 데이터가 유효한 경우, 서버에 업데이트 요청을 보냅니다.
            const response = await fetch("https://example.com/updateUser", {
              method: "POST",
              body: JSON.stringify(formData),
            });
            const data = await response.json();
        
            dispatch(updateUser(data));
          } catch (error) {
            // Yup 검사에서 오류가 발생한 경우, 에러를 dispatch하여 상태를 변경합니다.
            dispatch({
              type: "user/updateError",
              payload: error.errors,
            });
          }
        };
        ```
        
    - **Zod** ( 헷갈려서 적어둠→TypeScript로 작성된 객체 스키마 및 유효성 검사 라이브러리 )
        
             장점
        
        - TypeScript와 함께 사용하기에 적합합니다. Zod는 TypeScript와 함께 사용하기에 적합한 라이브러리
        
        단점
        
        - JavaScript와 함께 사용하기에는 부적합합니다. Zod는 TypeScript와 함께 사용하기에 적합한 라이브러리입니다. JavaScript와 함께 사용하는 경우에는, 타입 정보가 없으므로 활용이 제한될 수 있습니다.
        - Yup보다 문서화가 부족합니다. Zod는 Yup보다 문서화가 부족한 편입니다. 문서화가 더 많아진다면 더욱 쉽게 사용할 수 있을 것입니다.