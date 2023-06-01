# [ Day ] React (5/31)

# `* Daily Study Planner *`

## To Do List

- [x]  TIL 작성(day)
- [x]  TIL 작성(트러블 슛팅)
- [x]  팀원 스터디

## Self Study

- [x]  1일 1커밋 실천

## **Study-groud**

- [ ]  

## 수 5/31

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
✏️ 기술 면접 있는 날!!!

</aside>

---

## 🧳  참고자료

[https://github.com/baeharam/Must-Know-About-Frontend](https://github.com/baeharam/Must-Know-About-Frontend)

[GitHub - JaeYeopHan/Interview_Question_for_Beginner: Technical-Interview guidelines written for those who started studying programming. I wish you all the best.](https://github.com/JaeYeopHan/Interview_Question_for_Beginner#면접에서-받았던-질문들)

---

## 🤔 문제 상황

- **<Image> 컴포넌트**
    
    ## **`<Image>` 컴포넌트**
    
    Next.js에서는 이미지를 사용할 때 Next.js 서버를 한 번 거쳐서 이미지 최적화를 한 다음 사용할 수 있도록 해 주는데요. 그래서 되도록이면 `<img>` 태그보다는 `<Image>` 컴포넌트를 사용하는 걸 권장합니다. `<Image>` 컴포넌트는 `next/image`에서 불러와서 사용합니다. 이때 반드시 크기가 있어야 하는데요. `width`와 `height` 값을 지정하거나 또는 `fill`이라는 Prop을 사용할 수 있습니다.
    
    ****`width`와 `height`를 사용하는 경우**
    
    ```jsx
    import Image from 'next/image';
    
    export default function Page() {
      return (
        <>
          <Image
            src="/images/product.jpeg"
            width={300}
            height={300}
            alt="상품 이미지"
          />
        </>
      );
    }
    ```
    
    ****`fill`을 사용하는 경우**
    
    ```jsx
    import Image from 'next/image';
    
    export default function Page() {
      return (
        <>
         <div
            style={{
              **position: 'relative',**
              width: '100%',
              height: '300px',
            }}
          >
            <Image
              src="/images/product.jpeg"
              **fill**
              alt="상품 이미지"
              style={{
                **objectFit: 'cover',**
              }}
            />
          </div>
        </>
      );
    }
    ```
    
- ****<Head> 컴포넌트****
    
    만약 사이트 전체에 공통으로 적용하고 싶다면 `/pages/_app.js` 파일에서 `<Head>` 컴포넌트를 활용해 보세요.
    
    ```jsx
    import Head from 'next/head';
    
    export default function Page() {
      return (
        <>
          <Head>
            <title>페이지 제목</title>
            <link rel="icon" href="/favicon.ico" />
          </Head>
          ...
        </>
      );
    }
    ```
    
    ```jsx
    //pages/_app.js
    import Head from 'next/head';
    
    export default function App({ Component, pageProps }) {
      return (
        <>
          <Head>
            <title>사이트 기본 제목</title>
            <link rel="icon" href="/favicon.ico" />
          </Head>
          <Component {...pageProps} />
        </>
      );
    }
    ```
    
- ****개발모드, 빌드, 실행 그리고 배포****
    
    명령어
    
    <aside>
    💡 npm run dev / yarn dev → 개발 모드 
    npm run start / yarn start → 운영 모드
    
    </aside>
    
    <aside>
    💡 yarn run build
    
    </aside>
    

[모의면접](https://www.notion.so/40901555ecab426d9e5fe23ace3fced9)