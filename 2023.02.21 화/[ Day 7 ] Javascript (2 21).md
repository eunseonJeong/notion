# [ Day 7 ] Javascript (2/21)

# `* Daily Study Planner *`

## To Do List

- [x]  TIL 작성(day)
- [x]  TIL 작성(트러블 슛팅)
- [ ]  TIL 작성(달력기록)
- [x]  팀원 스터디

## Self Study

- [x]  1일 1커밋 실천

## **Study-groud**

- [ ]  

## 화  2/21

⏱️ **Study Time ::  16H 10M**

- [ ]  09:00 - 12:00 데이터 타입,실행 컨테스트 공부
- [ ]  12:00 - 13:00 점심 시간
- [ ]  13:00 - 19:30 개념 공부
- [ ]  19:00 - 20:00 저녁 시간
- [ ]  20:00 - 21:30 문제풀이 세션
- [ ]  21:30 - 11:00 css 문제풀기
- [ ]  11:00-00:30 모던 자바스크립트 예제 공부
- [ ]  00:30~01:00 TIL 작성

---

## 🗂️ React 숙련 시작!

## 금

- [x]  배열함수 영상보기
- [ ]  if함수 예제 풀기
- [ ]  MDN 예제 풀기

>하루종일 코테 하느라 
바빴다 ㅜ 아무것도 못함..

## 토

- [x]  코딩테스트 완료
- [x]  코딩테스트 복습
- [ ]  .map 활용

## 일

- [ ]  Break time

## 월

- 모던자바스크립트
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

- 모던자바스크립트
    - [ ]  map
    - [ ]  filter
    

## 수

- [x]  코딩테스트1
- [x]  코딩테스트2
- [ ]  코딩테스트3
- [ ]  코딩테스트4
- [ ]  if 함수
- [x]  삼항연산자

## 목

- [x]  코딩테스트3
- [x]  코딩테스트4
- [ ]  배열함수 영상이라도 보기
- [ ]  스코프
- [ ]  .map
- [ ]  if문

---

## 🗂️ **Study-groud**  :

---

## 🙂  오늘 어땠니?

<aside>
✏️   마음을 다시 잡았다. 남들과 나를 비교하지 말자. 흔들리지 말자. 나는 나만의 속도를 지키면서 불안해 하지말자. 조급해 하지 말자. 아직 늘어갈 타이밍이 아니지 않은가 나는 왜? 아직 여기에 머물러있지? 그렇게 생각하진 말자!

</aside>

---

## 🧳  내일 할 것들

- 자바스크립트 공부하기

---

## 🤔 문제 상황

- 스코프
    
    ```jsx
    var x = 10;
    
    function foo(){
    var x = 100;
    console.log(x);
    
    function bar(){   // 내부함수
    x = 1000;
    console.log(x); // ?
    }
    
    bar();
    }
    foo();
    console.log(x); // ?
    ```
    
- css
    
    ![css1.JPG](%5B%20Day%207%20%5D%20Javascript%20(2%2021)%2046d4db4e709d48dfa3d7bdb9f724e150/css1.jpg)
    
    ```jsx
    html {
        background-color: orange;
        height: 100%;
        width: 100%;
      }
      .whole{
        background-color: yellow;
        height: 300px;                      //%로 하면 안되고 px로 하면 된다 왜?? 가장 바깥쪽에 있는 부분은 px로 그 안은 %로 가능
        width: 300px;
      
        border: 1px solid black;
      }
    ```
    
    ```jsx
    	display: flex; 
      flex-direction: column;
      justify-content: space-evenly;(세로)
      align-items: center;(가로)
    ```
    
    ```jsx
    	display: flex; 
      flex-direction: row;
      justify-content: center;(가로)
      align-items: center;(세로)
    ```
    
    나는 `margin auto;`를 사용하였는데 저렇게 기본 값이 있을줄이야! 다음에 꼭 써야지 ㅎㅎ
    

map 예제 풀어보기

```jsx
const numbers = [1,4,9];
const roots = numbers.map(item => Math.sqrt(item));
// =const roots = numbers.map(Math.sqrt;)
console.log(roots);
console.log(numbers);

//새로운 함수 지정해줘서 거기에 새로운 배열 값 만들기!
```

filter 예제 풀어보기

```jsx
const numbers = [1,2,3,4,5,6];
const odds = numbers.filter(item => item % 2)
```