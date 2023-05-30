# [ Day ] React (5/24)

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

## 수 5/24

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
✏️ 오늘 팀스파르타 면접을 봤어. 면접 후기는 따로 작성해뒀당…. 후하 기술면접과 줌 면접 자체가 처음이었는데 나름 잘 끝낸것같아서 너무 수고했다라는 말을 해주고 싶네! 고생했어! 앞으로 있는 면접 기회에 최선을 다해보자!!!

</aside>

---

## 🧳  참고자료

---

## 🤔 문제 상황

[항해 면접질문](https://www.notion.so/18b4a2c8efd04988ba8e5125cc173629)

- Flexidesk 프로젝트
    - 드래그앤드롭 (useDADBox)

```jsx
import { useRef } from 'react';
import { useDispatch } from 'react-redux';
import { __editBox } from '../../../redux/modules/spaceBoxSlice';

export function useDADBox(spaceId, boardEl, boxList) {
  const dispatch = useDispatch();
  const elRef = useRef([]);

  const boxMouseDownHandler = (e, boxIndex) => {
    //마우스 클릭 좌표
    const mouseX = e.clientX;
    const mouseY = e.clientY;

    const boxMoveHandler = e => {
      const currentBox = boxList[0].find(box => box.boxId === boxIndex);
      //브라우저 기준,스크롤 x
      const newMouseX = e.clientX;
      const newMouseY = e.clientY;

      const mrDiffX = mouseX - currentBox.x;
      const mrDiffY = mouseY - currentBox.y;
      //현재 마우스 위치에서 이전 위치와의 차이를 뺀 값
      const newx = newMouseX - mrDiffX;
      const newy = newMouseY - mrDiffY;
      //요소의 경계 사각형 정보
      const boardRect = boardEl.current.getBoundingClientRect();
      //ref를 사용하여 실제 DOM 요소에 접근
      const boxRect = elRef.current[boxIndex].getBoundingClientRect();
      //화면 보드 경계를 벗어나지 않도록 함
      const limitedX = Math.max(
        boardRect.x - (boardRect.x + 10),
        Math.min(newx, boardRect.right - (boxRect.width + (boardRect.x + 10))),
      );
      const limitedY = Math.max(
        boardRect.y - (boardRect.y + 10),
        Math.min(
          newy,
          boardRect.bottom - (boxRect.height + (boardRect.y + 10)),
        ),
      );
      const payload = {
        spaceId,
        boxId: currentBox.boxId,
        boxName: currentBox.boxName,
        x: Number(limitedX),
        y: Number(limitedY),
      };
      return payload;
    };
    //함수는 마우스 업 이벤트를 처리 및 이동결과 처리
    const boxMouseUpHandler = (e, boxIndex) => {
      document.removeEventListener('mousemove', boxMoveHandler);
      document.removeEventListener('mouseup', boxMouseUpHandler);
      const result = boxMoveHandler(e, boxIndex);
      dispatch(__editBox(result));
    };
    //드래그 동작을 시작할 때 해당 이벤트를 처리하기 위해 등록
    document.addEventListener('mousemove', boxMoveHandler);
    document.addEventListener('mouseup', boxMouseUpHandler);
  };
  return {
    elRef,
    boxMouseDownHandler,
  };
}
```

마우스 클릭좌표에 대한 선택

```jsx
//마우스 클릭 좌표
    const mouseX = e.clientX;
    const mouseY = e.clientY;
```

종류

**client** 메서드는 브라우저가 기준인 좌표입니다. 현재 보이는 브라우저 화면 상에서 어느 지점에 위치하는 지를 의미하기 때문에 스크롤 해도 값은 변하지 않습니다.

**offset** 메서드는 이벤트가 걸려 있는 DOM객체를 기준으로 좌표를 출력합니다. 이와 비슷한 메서드로 layer가 있습니다. 이 메서드는 현재 파이어폭스에서만 사용합니다.

**screen** 메서드는 화면 출력 크기(자신의 모니터)가 기준인 절대 좌표입니다. 브라우저를 움직여도 값은 같습니다.

**page** 메서드는 문서가 기준입니다. client와 비슷하지만 이 메서드는 문서 전체 크기가 기준이라 스크롤 시 값이 바뀝니다. (스크롤을 포함해서 측정합니다)

이유

브라우저가 기준으로 봐야 값을 특정할 수 있었으며 스크롤 값이 변하지 않아야 했기 때문에 client를 사용

웹 브라우저에서 실행되므로 사용자가 요소를 드래그하고 놓는 등의 동작을 감지하고 이에 대한 처리를 수행

- 참고
    
    [[Javascript] 마우스 이벤트 / 드래그 앤 드롭 (Drag and drop)](https://velog.io/@task11/Javascript-마우스-이벤트-드래그-앤-드롭-Drag-and-drop)
    
    [](http://megaton111.cafe24.com/2016/11/29/clientx-offsetx-pagex-screenx의-차이점/)
    
- 나도  도형 드래그앤 드롭 구현 해봤다아
    
    ```jsx
    import { useRef, useState } from "react";
    
    export default function Test() {
      const containerRef = useRef(null); // 드래그 할 영역 네모 박스 Ref
      const dragComponentRef = useRef(null); // 움직일 드래그 박스 Ref
      const [originPos, setOriginPos] = useState({ x: 0, y: 0 }); // 드래그 전 포지션값 (e.target.offset의 상대 위치)
      const [clientPos, setClientPos] = useState({ x: 0, y: 0 }); // 실시간 커서위치인 e.client를 갱신하는값
      const [pos, setPos] = useState({ left: 0, top: 0 }); // 실제 drag할 요소가 위치하는 포지션값
    
      const handleDragStart = (e) => {
        const { offsetLeft, offsetTop } = containerRef.current;
        const { clientX, clientY } = e;
        setOriginPos({ x: clientX - offsetLeft, y: clientY - offsetTop });
        setClientPos({ x: clientX, y: clientY });
      };
    
      const handleDrag = (e) => {
        const { clientX, clientY } = e;
        const { x: originX, y: originY } = originPos;
        const deltaX = clientX - clientPos.x;
        const deltaY = clientY - clientPos.y;
        setClientPos({ x: clientX, y: clientY });
        setPos({ left: originX + deltaX, top: originY + deltaY });
    
        console.log("deltaX", deltaX);
        console.log("deltaY", deltaY);
    
        console.log("clientX", clientX);
        console.log("clientY", clientY);
      };
    
      const handleDragEnd = () => {
        setOriginPos({ x: 0, y: 0 });
        setClientPos({ x: 0, y: 0 });
      };
    
      return (
        <div
          ref={containerRef}
          style={{ position: "relative", width: "500px", height: "500px" }}
        >
          <div
            ref={dragComponentRef}
            style={{
              position: "absolute",
              left: pos.left,
              top: pos.top,
              width: "100px",
              height: "100px",
              background: "red",
            }}
            draggable="true"
            onDragStart={handleDragStart}
            onDrag={handleDrag}
            onDragEnd={handleDragEnd}
          ></div>
        </div>
      );
    }
    ```