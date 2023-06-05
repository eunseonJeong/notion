# [ Day ] React (4/4)

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

## 화 4/4

⏱️ **Study Time ::  17H 00M**

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

- [ ]  Yup ( 유효성검사 정규식 라이브러리) 공부
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
- [ ]  이메일 인증 체크
- [ ]  마이다스 역검
- [ ]  코테 2문제 풀기

## 수

- [ ]  이메일 인증 체크
- [ ]  회원가입 시 이름은 중복 체크 안되어있음! 어떻게 하면 좋을지 생각해보기
- [x]  Yup ( 유효성검사 정규식 라이브러리) 공부
    - [x]  이메일
    - [x]  아이디
    - [x]  비밀번호
- [ ]  로그인 요청에 대한 상태를 만들어서 isSuccess 할때 alert 띄우는 식으로 변경해보기
- [x]  코테 2문제 풀기

## 목

- [x]  이메일 인증 체크

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
✏️ 기능 구현은 끝냈다!!! 하지만 오류처리와 정규식처리를 아직 못했다 ㅜㅜ 오늘 하루종일 서버가 깜빡거려서 테스트하는데 됐다 안됐다가 반복이었던것같다 .. ㅜㅜ

**주석인 코드를 아까워하지 말자..**

</aside>

---

## 🧳  내일 할 것들

- [ ]  

---

## 🤔 문제 상황

- 트러블 슈팅
    
    
    ```jsx
    const onsumbitHandler = async e => {
        e.preventDefault();
        try {     
          const response = await api.post('/users/login', user);
          const token = response.headers.authorization
          const newtoken = token.split(" ")[1]
          const payload = jwt_decode(newtoken);
          **~~const decode = jwt_decode(payload.id);~~**
          cookies.set('token', response.headers.authorization, { path: '/' });
          **cookies.set('userId', response.headers.authorization.id, { path: '/' });**
          navi('/');
        } catch (e) {
          const errorMsg = e.response.data.message;
          alert(`${errorMsg}`);
        }
      };
    
    /////////////////////////////////////////////////////////////////////////////////////
    const onsumbitHandler = async e => {
        e.preventDefault();
        try {     
          const response = await api.post('/users/login', user);
          const token = response.headers.authorization
          const newtoken = token.split(" ")[1]
          const payload = jwt_decode(newtoken);
          console.log(payload);
          console.log("너 토큰이야!!!!!!!!",newtoken);
          cookies.set('token', response.headers.authorization, { path: '/' });
          **cookies.set('userId', payload.id, { path: '/' });**
          navi('/');
        } catch (e) {
          const errorMsg = e.response.data.message;
          alert(`${errorMsg}`);
        }
      };
    ```
    
    상황: 서버에서 token안에 보내준 userId값을 받아와서 cookies에 저장해줘야함. 근데 자꾸 undifiend만 뜨고 값이 없다네?
    
    내가 생각해 본 부분:  try 안에서 뭐하나라도 잘못되면 catch가 실행
    내 생각엔 ‘payload 자체가 token 이다?’ 라고 대답했는데 응 아니야 ~
    **jwt_decode는 jwt만 들어갈 수 있다.. !**
    
    jwt 안에 있는 payload를 꺼내는 함수이기 때문에, 다른 값이 들어가면 invalid token이라고 에러가 납니다.
    payload에 있는 id를 쿠키에 저장! 그래서 jwt_decde에서 아까 에러가 나서 catch로 이동.
    
    결과: 
    **`cookies.set('userId', payload.id, { path: '/' });` 으로 바꿔주니 값도 잘 담기고 해결이 완료 되었다.**