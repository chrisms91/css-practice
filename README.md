# css-practice

Practicing CSS (Flexbox, Grid...)

### **#1. FlexBox**

  - Father 에게 명령한 규칙은 children items들에게 영향을 끼치게 된다
  - 수평정렬: justify-content, 수직정렬: align-items
  - display: flex 를 하면 flex-direction: row is default. When you change flex-direction, main and cross axis are also changed.
    - flex-direction: row -> main(수평) / cross(수직)
    - flex-direction: column -> main(수직) / cross(수평)
  - align-self: works on single item

### **#2. Grid**

  - **Grid has similar things to flexbox.**
    - grid-auto-direction: row is defualt -> 정의되지 않은 elements에 대해서는 row에 자동으로 놓는다.

  - **grid-template-ares + grid-area: you can draw the grid. need a size -> use grid-auto-rows or columns**
    - divs find a proper place to put without setting width, height or top...

    ```css
    .father {
       display: grid;
       grid-auto-rows: 100px;
       grid-gap: 10px;
       grid-template-columns: repeat(5, 1fr);
     }
    ```

  - **grid has new measurement unit: fr (fraction)**
    - repeat(): set same size for all columns
    - minmax(): control minimum / maximum size of content
    - min-content: 가능한 적게 자리를 차지할 수 있게 해줌
    - max-content: 가능한 자리를 많이 차지할 수 있게
    - auto-fill: 가능한 많은 cell로 container를 꽉 채움 (creating ghost grid)
    - auto-fit: 빈자리를 채울때까지 expand.
      - repeat(auto-fill, minmax(350px, 1fr));

  - **grid also have justify-content, alogn-content...like flexbox**
    - place-content:  align-content + justify-content 

  - **place-content는 box자체를 움직임, place-items는 박스 안의 content를 움직임**

  - **grid-column: determine grid item's size**
    - grid-column: 1 / 3 -> this grid will be from line 1 to line 3 (line으로 계산한다.)
    - grid-column-end: -1 -> 라인 전체를 차지합니다. (라인수를 세기 귀찮을 때)
    - grid-auto-flow: dense -> 빈칸을 땡겨 채울 수 있다 (자주 사용 안함..)

  - box 안 첫번째 자식에게 1 부터 5까지 가져가라고 명령하는 것.
```css
.box:first-child {
  grid-row: 1 / 5
}
```
- span을 써서 더 편하게 사용 가능.
```css
.box:first-child {
  grid-row: span 5
}
```

- Row Start / Column Start / Row End / Column End
```css
.box:first-child {
  grid-area: 2 / 1 / 4 / -1;
}
```



### **#3. PostCSS / CSSNext / CSS4**
- Parcel
  - Like es6 is being transformed to es5 through barbel, parcel let us using modern CSS functionalities (CSS4)
  - Parcel 공식 홈페이지: https://ko.parceljs.org

- PostCSS
  - A tool for transforming CSS with JavaScript

- Funtional Pseudo Selectors
  > look into the document for more feature
  - matches(), not()
    - 해당되는 속성을 넣어주면 적용 / 제외 시킴.
  ```css
  li:matches(:nth-child(even), .target) {
    /* 짝수번째 li들 + li with target class 선택 */
    background-color: blue;
  }

  li:not(.target) {
    /* target클라스 element 제외 */
    background-color: blue;
  }
  ```
