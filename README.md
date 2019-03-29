# css-practice

Practicing CSS (Flexbox, Grid...)

### #1. FlexBox

  - Father 에게 명령한 규칙은 children items들에게 영향을 끼치게 된다
  - 수평정렬: justify-content, 수직정렬: align-items
  - display: flex 를 하면 flex-direction: row is default. When you change flex-direction, main and cross axis are also changed.
    - flex-direction: row -> main(수평) / cross(수직)
    - flex-direction: column -> main(수직) / cross(수평)
  - align-self: works on single item

  ### #2. Grid

  - Grid has similar things to flexbox.
    - grid-auto-direction: row is defualt -> 정의되지 않은 elements에 대해서는 row에 자동으로 놓는다.
  - grid-template-ares + grid-area: you can draw the grid. need a size -> use grid-auto-rows or columns;
    - divs find a proper place to put without setting width, height or top...
  -grid has new measurement unit: fr (fraction)
    - repeat() -> set same size for all columns
    - minmax() -> control minimum / maximum size of content
