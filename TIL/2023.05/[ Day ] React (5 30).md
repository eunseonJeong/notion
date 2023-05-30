# [ Day ] React (5/30)

# `* Daily Study Planner *`

## To Do List

- [x]  TIL 작성(day)
- [x]  TIL 작성(트러블 슛팅)
- [x]  팀원 스터디

## Self Study

- [x]  1일 1커밋 실천

## **Study-groud**

- [ ]  

## 화 5/30

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

[데일리 과제](https://www.notion.so/78826840e9644b31b2b5ea0865a11318)

---

## 🙂  오늘 어땠니?

<aside>
✏️ 오늘부터 이력서 코칭 및 기술 면접 과정이 시작되었다! 그리고 팀원들과 함께 면접 스터디를 진행하면서 몰랐던 부분과 알고 있었지만 정확하게 몰랐던 부분을 알게되면서 공부가 많이 되었다. 모르는 부분 또는 잘 이해가 가지 않는 부분은 피그마에 그려가면서 정리를 하니 잘 이해가 되었고 그래도 명확하지 않은 부분들은 예시를 통해 직접 보거나 구현해보면서 알게되었다.

</aside>

---

## 🧳  참고자료

[https://github.com/baeharam/Must-Know-About-Frontend](https://github.com/baeharam/Must-Know-About-Frontend)

[GitHub - JaeYeopHan/Interview_Question_for_Beginner: Technical-Interview guidelines written for those who started studying programming. I wish you all the best.](https://github.com/JaeYeopHan/Interview_Question_for_Beginner#면접에서-받았던-질문들)

---

## 🤔 문제 상황

### Next.js에서 외부 이미지 사용 시 설정하는 방법

오류 발생: 외부 이미지를 사용했을 때의 에러 코드가 뜸

```jsx
Error: Invalid src prop (https://learn-codeit-kr-static.s3.ap-northeast-2.amazonaws.com/codeitmall/product-09.png) on `next/image`, hostname "learn-codeit-kr-static.s3.ap-northeast-2.amazonaws.com" is not configured under images in your `next.config.js`
See more info: https://nextjs.org/docs/messages/next-image-unconfigured-host
```

해결방안: 이때 [https://nextjs.org/docs/messages/next-image-unconfigured-host](https://nextjs.org/docs/messages/next-image-unconfigured-host) 사이트 접속 후 복사 → next.config.js 파일에 붙여넣기 !!

```jsx
// next.config.js
module.exports = {
  images: {
    remotePatterns: [
      {
        protocol: 'https',
// 에러에서 친절하게 hostname "learn-codeit-kr-static.s3.ap-northeast-2.amazonaws.com" 적으라고 알려준다.
        hostname: 'assets.example.com',
        port: '',
//codeitmall을 적어준다.
        pathname: '/account123/**',
      },
    ],
  },
}
```