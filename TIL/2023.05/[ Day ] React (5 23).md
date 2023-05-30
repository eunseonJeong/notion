# [ Day ] React (5/23)

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

## 화 5/23

⏱️ **Study Time ::  17H 30M**

- [ ]  

---

## 🗂️ React 숙련 시작!

## 금

## 토

## 일

- [ ]  

## 월

- [x]  

## 화

- [x]  

## 수

- [x]  

## 목

- [ ]  

---

## 🗂️ **Study-plan**  :

면접준비 기간

---

## 🙂  오늘 어땠니?

<aside>
✏️ cs 지식을 공부했다. 자바스크립트를 배울때 지나쳐갔던 개념들에 대해서 조금더 명확하게 와닿을 수 있었다.

</aside>

---

## 🧳  참고자료

---

## 🤔 문제 상황

**useEffect에 객체를 넣으면 ?**

```jsx
const [data, setData] = useState({ name: "John", age: 30 });

  useEffect(() => {
    setData({ name: "Jane", age: 30 });
    console.log("error");
  }, [data]);
> 결과 : 무한 렌더링 발생
> 이유 : 이것은 useEffect의 디펜던시(의존성 배열)로 data 객체를 전달하고 있지만, useEffect 내부에서 setData를 통해 data 객체를 변경하고 있기 때문
객체는 참조 타입이므로 setData로 객체를 변경하면 새로운 객체가 생성되고 data의 참조가 업데이트 됨 . 디펜던시에 값을 비워주면 렌더링이 최초 한번만 됨.
```

**git 에러**

에러 메세지: `fatal: will not add file alias`

원인: 커밋할 때 수정하기 전 파일 이름과 수정후의 파일 이름의 대소문자 ignorecase때문에 생기는 오류

해결: `git config --local core.ignorecase false`