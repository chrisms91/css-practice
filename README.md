# css-practice

Practicing CSS (Flexbox, Grid...)

### CSS Flex

- #1.1 Basics
  - Father 에게 명령한 규칙은 children items들에게 영향을 끼치게 된다
  - 수평정렬: justify-content, 수직정렬: align-items
  - display: flex 를 하면 flex-direction: row is default. When you change flex-direction, main and cross axis are also changed.
    - flex-direction: row -> main(수평) / cross(수직)
    - flex-direction: column -> main(수직) / cross(수평)
  - align-self: works on single item