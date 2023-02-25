# [ Day 2 ] Javascript (2/16)

# `* Daily Study Planner *`

## To Do List

- [x]  TIL 작성(day)
- [ ]  TIL 작성(트러블 슛팅)
- [x]  TIL 작성(달력기록)
- [x]  팀원 스터디
- [x]  배열과 관련한 메서드 알아보기

## Self Study

- [x]  1일 1커밋 실천
- [ ]  

## **Study-groud**

- [x]  전역 스코프
함수 스코프 -은선
- [x]  .map() .filter()-주희
map은 중간정도만 이해함
- [x]  Array -철환

## 목  2/16

⏱️ **Study Time ::  16H 34M**

- [ ]  09:00 - 10:00 어제 못올린 것 올리고 스터디 방 추가 수정하기
- [ ]  10:00 - 11:30 코딩테스트3
- [ ]  11:30 - 12:30 낮잠 zZ
- [ ]  12:30 - 13:30 코딩테스트 바탕으로 개념 공부하기
- [ ]  13:30 -14:00 점심시간
- [ ]  14:00~16:00 코딩테스트 4
- [ ]  16:00~19:00 코딩테스트 5
- [ ]  19:00 - 19:30 저녁시간
- [ ]  19:30 - 21:00 이윤 매니저님 순회
- [ ]  21:00 - 22:30 전체적인 TIL
- [ ]  22:30~01:00 스터디 팀원들과 개념 알아오고 설명하기
- [ ]  01:00 - 01:30 코드 정리한 것 다시 확인해보기, TIL 정리

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
✏️   오늘은 코딩테스트를 3개 풀었는데 if랑 for문을 사용하지 않고 진행하려고 노력했다.(왜냐면.. 난 조건 반복문을 잘 못ㅅ써서 ㅜㅜ ) 근데 뭔가 잘 되지 않아서 너무 속상했다.. 더 공부를 해야겠다고 느꼈다.!!! ㅜㅜ 아직 나는 부족하다. 그래도 조원 분이 늘어가고 있는게 보이고 이제 개념이 슬슬 잡히는게 눈에 보인다고 말해줘서 난 오늘도 한걸음 더 나아갈 수 있는 사람이 된 것 같다. **개발은 묵묵하게 쭉 밀고 나가는 것.**

</aside>

---

## 🧳  내일 할 것들

- 코딩 테스트…. 월요일 시험 준비 해야된단다 ~
- 예제 풀어보기

[W3Schools Java Exercise](https://www.w3schools.com/java/exercise.asp?filename=exercise_math2)

- <스터디>
    - 개념정리 스터디
    - 임건님과 아이들 스터디
    - 김동찬님과 코딩프로젴젴

---

## 문제 상황

- Math.abs
    1. 문제 상황
    - Math.abs의 문법을 잘 적었다고 생각하는데 실행이 안되는 상황
    
    ```jsx
    //숫자 배열 후 더하기는 함수찾기> 평균합 구하는 방법: (첫번째 숫자+끝 숫자)/2 + 원래 숫자 곗수//
    //작성코드
    function adder(a, b){
    var result = 0
    
    return (a+b)*(Math.abs(b-a)+1)/2;
    
    }
    ----------------------------------------------------------------------------------------------------------------------------------------------------------
    //코테에는 지정된 함수값 function을 adder대신 넣어줘야 실행된다!!!
    //해결완료
    function solution(a, b){
        var result = 0
        
        return (a+b)*(Math.abs(b-a)+1)/2;
    
    }
    
    ```
    
    > 2. 내가 생각하는 핵심 에러 메세지
    > 
    - type error
    
    > 3. 나의 시도
    > 
    - type??/ 뭔가 선언이 되어있지 않았나? 대체 뭘까?
    - 값이 잘못된걸까? 괄호가 잘못되어있나? 체크함
    
    > 4. 참고한 레퍼런스
    > 
    - [https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Math/abs](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Math/abs)
    - [https://m.blog.naver.com/PostView.nhn?blogId=saomath&logNo=222046532714&proxyReferer=https:%2F%2Fwww.google.com%2F](https://m.blog.naver.com/PostView.nhn?blogId=saomath&logNo=222046532714&proxyReferer=https:%2F%2Fwww.google.com%2F)
    
    > 5. 이후 상황
    > 
    - solution으로 바꿔주니 바로 실행되었고, 다른 곳에서 사용하면 solition값을 변경해줘도 되지만 코테에선 지정된 값만 사용해줘야 하기 때문에 오류가 났었던 것이다 !!!
    - 사실 이 부분은 기록을 할까말까 고민했는데 너무 어이없는 실수라 그러지말자고 기록해둔다.. 오타 함수명 다시 한번 재확인 하는 습관을 가지자!!!!