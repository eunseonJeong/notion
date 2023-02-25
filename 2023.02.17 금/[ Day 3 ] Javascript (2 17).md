# [ Day 3 ] Javascript (2/17)

# `* Daily Study Planner *`

## To Do List

- [x]  TIL 작성(day)
- [x]  TIL 작성(트러블 슛팅)
- [x]  TIL 작성(달력기록)
- [x]  팀원 스터디
- [ ]  배열과 관련한 메서드 알아봐서 토큰에 메모

## Self Study

- [ ]  1일 1커밋 실천
- [ ]  

## **Study-groud**

- [x]  코딩 테스트

## 금  2/17

⏱️ **Study Time ::  12H 00M**

- [ ]  09:00 - 12:00 코딩테스트 풀기
- [ ]  12:00 - 13:00 점심시간
- [ ]  13:00 - 19:30 코딩테스트 풀기
- [ ]  19:30 - 20:30 저녁시간
- [ ]  20:30 - 21:30 예상기 매니저님 순회
- [ ]  21:30 - 00:30 코딩테스트 풀기
- [ ]  00:30~01:30 TIL 쓰고 Git 올리기
- [ ]  01:30 - 03:00 코딩테스트에서 사용한 문법 복습

---

## 🗂️ React 숙련 시작!

## 금

- [ ]  배열함수 영상보기
- [ ]  if함수 예제 풀기
- [ ]  MDN 예제 풀기

>하루종일 코테 하느라 
바빴다 ㅜ 아무것도 못함..

## 토

- [ ]  코딩테스트 완료
- [ ]  코딩테스트 복습
- [ ]  .map 활용

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
✏️   나 자신을 못 믿는 상황이 너무 많았어 ㅜㅜ.. 분명 내 코드에 자신감을 가지고 해야되는데 아직 확실하지 않아서 그런지 말에 물음표가 많네 ㅜㅜ 그걸 좀 자신있게 이야기하고 자신있게 설명할 수 있는 내가 되었으면 좋겠어! 그러려면 잘 알아야겠지? 그러기위해선 개념공부.. 그리고 복습을 꾸준히 하자 ㅜㅜ 그러면 나도 될거야! 할 수 있다 !!! 아 그리고 코딩 테스트를 하니 내가 배운 기능을 쓰기도 하고 새로운 기능도 알 수 있어서 개념 공부에 도움이 되는 것 같다 ㅎㅎ 오늘 오후엔 머리가 과부화 될 만큼 했으니 꼭 복습하고 잡시다요

</aside>

---

## 🧳  내일 할 것들

- 코딩 테스트…. 월요일 시험 준비 해야된단다 ~
- 예제 풀어보기

[W3Schools Java Exercise](https://www.w3schools.com/java/exercise.asp?filename=exercise_math2)

- <스터디>
    - 개념정리 스터디
    - 김동찬님과 코딩프로젴젴

---

## 🤔 문제 상황

## 보통 오타, 괄호, 변수명 확인 !!! , **초기값 설정(문자, 숫자, 배열 등)** **초기값에 더해주고 어떻게 해보자.**

- 1 repeat 사용
    
    > 1. 변수명을 확인해주지 않아서 오류가 계속 났던 문제
    > 
    
    ```jsx
    // n의 숫자만큼 배열이 추가가 됨!
    //변수명... 제발............ 확인하자..
    //repeat = 동일한 문제 계속 붙이기
    
    function solution(n) {
        var srt = '수박';              //['수박']이라고하면 안되나? yes 된다
                                        //수박수라고 찍혀야되서 안되는건가?
        if(n % 2 === 0){
            return srt.repeat(n/2);     //수박이 몇번들어가는지 확인하자!
        } else {
            return srt.repeat(n/2)+'수';
        }
        console.log(n)
    }
    ```
    
    > 2. 내가 생각하는 핵심 에러 메세지
    > 
    - 
    
    > 3. 나의 시도
    > 
    - n의 값을 대입해봐서 생각 정리 다시 해주기
    - 어디에 들어가야 하는지 **srt의 값**을 정확하게 넣어주기
    - n=5이면 자릿수가 5니깐 ‘수박수박수’ 로 나올것이고 수박이라는 단어는 2번 들어가게 되며 뒤에 ‘수’만 붙이면 해결되는 문제
    - `srt.repeat(n/2)+'수';` 를 봤을때 repeat() 안에는 문자를 넣지 못해요
    
    > 4. 참고한 레퍼런스
    > 
    - [https://www.codingfactory.net/10916](https://www.codingfactory.net/10916)
    
    > 5. 이후 상황
    > 
    - 해결완료
    
- 2 indexOf 특정 변수명 찾기
    
    ```jsx
    //문자형배열 서울의 김의 위치를 x찾아라
    //index는 순회하다가 찾으면 끝난다!
    function solution(seoul) {  
        kimIndex = seoul.indexOf('Kim')
        return "김서방은 " + kimIndex + "에 있다"
    }
    
    //findIndex는 모두 다 순회 후 찾는다
    function solution(seoul) {
    let h = seoul.findIndex(e => e == "Kim")
    return '김서방은 ' + h + '에 있다';
    }
    
    findIndex 순회 하심 e 그 안에 배열을 가르킨다.
    그 때 해당 e 고게 KIM 이랑 같으면 가져온다
    시간복잡도가 안 좋음
    ```
    
- 3 if문
    
    ```jsx
    //count가 올라가는 만큼 price도 올라감
    //곱하기 연산자 이용하기 price * count(이용한 만큼)
    //크거나 같거나를 꼭 넣어줘야한다.
    //i의 조건값 확인하기
    
    function solution(price, money, count){
        let needMoney = 0;
        for(i = 1; i <= count; i++){
            needMoney += (i * price)
        }
        return money > needMoney ? 0 : needMoney - money;
    }
    ```
    
     2. 내가 생각하는 핵심 에러 메세지
    
    - `needMoney += (i * price)` 이 부분이 막혔다 .
    - 질문을 잘 이해하자 !!!
    
    > 3. 나의 시도
    > 
    - for 안에 있는 i의 조건값 부등호 변경
    - `i =0;`으로 해두었는데 `i=1;`로 바꾸니 되었다
    
    > 4. 참고한 레퍼런스
    > 
    - 
    
    > 5. 이후 상황
    > 
    - 해결완료
- 4 제곱근 사용
    
    ```jsx
    //제곱근 사용 pow? sqrt? > Math.sqrt([대상 숫자]);라 sqrt사용
    //n에서 +1을 한 값에 return이 되야한다.
    //**제곱을 나타냄 간단히 사용가능
    //변수명..
    
    function solution(n) {          
        let num = Math.sqrt(n);     
        // let num = n을 제곱근으로 만들어줘야함. 그래야 -1이 나옴
        return Number.isInteger(num) ? (num+1)**2 : -1; 
    }
    ```
    
- 5 특정 요일 찾기
    
    ```jsx
    //js날짜 함수고민
    //a,b를 가지고 요일찾기
    //let day = new Date(a-1,b); a-1을 사용하는 이유는 일요일=-1 월요일 =1
    //디테일 확인하기.. 2016년도 안써줬다.. 이 문제가 2016년인데 .말이 안된다
    //인자로 뭐가 들어가는지 확인하기 !!! 몇개 ? 뭐 이런것들
    
    function solution(a, b) {
    let day = new Date(2016,a-1,b);
         const WEEKDAY = ['SUN', 'MON', 'TUE', 'WED', 'THU', 'FRI', 'SAT'];
         let week = WEEKDAY[day.getDay()];
         return week
    }
    ```
    
    >2016을 안적어줘서 에러가 났던 상황
    
    >년도를 기입해줘야 정확한 요일이 나온다
    
    >`const WEEKDAY = ['SUN', 'MON', 'TUE', 'WED', 'THU', 'FRI', 'SAT'];` 이것도 빼먹지 말자궁~
    
- 6 String(n).split('').sort().reverse();
    
    ```jsx
    //내림차순인데 자릿수 확인하기
    //리턴값은 오름차순
    //sort() - 배열을 정렬/reverse() - 원소 순서를 반대로
    //n.숫자 >문자>배열>sort>reverse>문자>숫자
    //숫자>문자 String(n);
    //문자>배열 str.split('')/sort
    //배열합치기 join('')
    
    function solution (n){
        let answer = []
        let str = String(n).split('').sort().reverse();     //문자로 바꿔주고,배열로바꾸고,
                                                            //배열정렬, 반대로
        for(let i =0; i< str.length; i++){
            answer.push(str[i])
        }
        return Number(answer.join(''))                      
    }
    ```
    
    ### >**String**(숫자를 문자로 변경해주는 형변환)**, split**(배열로 바꿔주는 형변화)**,sort**(배열정렬),**reverse**(반대로)
    
    각 어떤건지는 알지만 ㅜ.. 어떻게 배열해서 써줘야할까 저렇게 쓰면 된다 !!!
    
    하고 push로 배열 합쳐주면 된다 ~
    
- 7 문자가 아니라 Number을 반환
    
    ```jsx
    //숫자를 배열 만들어주기 .reverse();
    //숫자>문자 String(n); 문자>배열 str.split('')
    
    //["12345"]> join도 넣어봤는데 12345이 나온다 왜??
    //문자가 아니라 Number을 반환해야함
    
    function solution(n) {
        let answer = [];
         let str = String(n).split('').reverse();       //랜덤으로 돌아가지 않으니 오름차순 x
         for(let i = 0; i < str.length; i++){
             answer.push(Number(str[i])) 
         }
          return answer;
    }
    ```
    
- 8 i의 조건설정오류
    
    ```jsx
    //자릿수의 합
    //배열안의 합
    //문자에서 숫자 바꿔주기
    //i = 1라고 입력해서 오류남 , i = 0이라고 입력해줘야 함
    
    function solution(n){
        let answer = 0;
        let str = String(n).split('')
        for(let i = 0; i < str.length; i++) {
            answer += Number(str[i]);
    }
        return answer
    ```
    
    `for(let i = 0; i < str.length; i++) {
            answer += Number(str[i]);` 에서 Number() 꼭 알아두기!!! 문자에서 숫자로 변경해줘야지~~~
    
- 9 초기값 설정 중요 !!! includes
    
    ```jsx
    // 객체 안에서 더해주는 방식
    //배열에 어떤 값이 들어있는지 확인할 때 includes()를 사용
    **//****초기값 설정**** 초기값에 더해주고 어떻게 해보자.**
    
    function solution(numbers) {
        var answer = 0;      
        for(i = 0; i < numbers.length; i++){
        answer += numbers[i];                   //어디에 더해야 하는지?
        }
        return 45 - answer;
    }
    
    // function solution(numbers) {
    // var answer = 0;
    //     for(let i=0; i < 10; i++){
    //         if(!numbers.includes(i)) answer += i;           //!하나 일때 false사용,
    //     }
    //     return answer;
    // }
    ```
    

---