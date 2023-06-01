# [ Day ] React (4/2)

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

## 일 4/2

⏱️ **Study Time ::  11H 30M**

- [ ]  

---

## 🗂️ React 숙련 시작!

## 금

- [ ]  

## 토

- [ ]  

## 일

- [ ]  

## 월

- [ ]  

## 화

- [ ]  
- [ ]  

## 수

- [ ]  

## 목

- [ ]  
- [ ]  

---

## 🗂️ **Study-plan**  :

### <최종 프로젝트>

1. 회원가입 ( 관리자 ) /users/signup/admin
'회사 관리자'는 메일 인증을 통해 고유 번호(companyName)를 받고 고유 번호를 직원들한테 뿌림 !

~~참고) [https://coding-hwije.tistory.com/6?category=856854](https://coding-hwije.tistory.com/6?category=856854)~~

[~~https://bb-library.tistory.com/106~~](https://bb-library.tistory.com/106)

## [**~~https://kibua20.tistory.com/80](https://kibua20.tistory.com/80)  → step 2부터 ... 이어서 해야해요..............~~**

1. 회원가입 ( 사원 ) /users/signup/user
고유 번호(companyName) 입력란이 있어야 함
2. 로그인 (관리자&사원) /users/login
가입 시 사용한 이메일, 패스워드 입력하면 됨

- ~~input 컴포넌트로 빼기 ok~~ (일단 로그인& 회원가입 + 마이페이지 ? 부분에서만 사용됨)
- navigate 컴포넌트로 빼기는 성공 ?! ㅇㅇ 사용해보기

```jsx
import { useHistory } from 'react';
 
function useNavigate() {
  const history = useHistory();

  function navigateTo(path) {
    history.push(path);
  }

  function navigateBack() {
    history.goBack();
  }

  return {
    navigateTo,
    navigateBack,
  };
}
export default useNavigate;
```

---

## 🙂  오늘 어땠니?

<aside>
✏️ 오늘은 역할분담을 하는 날이었어. 나는 로그인,회원가입을 맡았어!! 이번엔 꼭 인증인가 뿌셔봐야지 ㅎㅎㅎ

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
    
    결과: api.js request에 토큰값이 포함이 되어있어서 서버연결이 실패되었던 것이었다.. 주석처리 해주니 말끔히 200으로 넘어감 ~ ~ ~ 
    
    ```jsx
    // instance.interceptors.request.use(
    //   // 요청을 보내기 전 수행되는 함수
    //   function (config) {
    //     const token = cookies.get("token")
    //     config.headers["authorization"] = `Bearer ${token}`;
    //     return config
    //   },
    
    //   // 오류 요청을 보내기 전 수행되는 함수
    //   function (error) {
    //     return Promise.reject(error)
    //     // return error 가 아님 !! 꼭 프로미스.리젝트 여야만 함
    //   }
    // )
    
    // instance.interceptors.response.use(
    //   // 응답을 내보내기 전 수행되는 함수
    //   function (response) {
    //     return response
    //   },
    
    //   // 오류 응답을 내보내기 전 수행되는 함수
    //   function (error) {
    //     return Promise.reject(error)
    //   }
    // )
    ```