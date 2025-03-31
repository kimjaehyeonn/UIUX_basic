# UI/UX 기초

### 1. UI/UX 기본개념

- **UI(User Interface)**
  : 사용자가 컴퓨터나 스마트폰, 웹사이트, 애플리케이션 등과 상호작용하는 방식

- **UX(User Experience)**
  : 사용자가 UI를 통해 얻는 경험.

### 2. Flexbox

**1/ 컨테이너 영역**

```
<!-- 기준이 되는 부모/컨테이너에 display:flex 적용 -->
display: flex;

<!-- 주축 방향 변경 -->
flex-direction: row/  row-reverse,column, column-reverse;

<!-- 부모/컨테이너 여역 부족 시 자동 줄바꿈 -->
flex-wrap: wrap / wrap-reverse;

<!-- flex-flow: flex-direction, flex-wrap 한꺼번에 쓰기 -->

<!-- 주축 방향 결정 -->
justify-content: center;
 /*
spacebetween:양쪽 맞추고 나머지 균일,
space-around: 아이템 하나 기준 양쪽 균일하게,
space-evenly: 여백을 기준 균일하게 */

<!-- 교차축 방향 결정 -->
align-items: center;
 /*
stretch: 기본값, 높이가 없을 때만 적용.
flex-start: 교차축 시작
flex-end: 교차축 끝
*/

<!-- align-content: center; wrap에 의해서 두줄로 되었을 때 -->
```

**2/ 아이템영역**

```
<!-- 컨테이너의 크기가 부족해도 아이템의 크기를 유지하도록 -->
flex-shrink: 0;

<!-- 컨테이너 공간이 남았을 때 여백을 차지하도록/비율대로 -->
flex-grow:1;
```

### 3. Grid

**1/컨테이너 영역**

```
display: grid;
<!-- 열 template  크기 지정 -->
grid-template-columns: repeat(3, 100px);

<!-- 행 template 크기 지정 -->
grid-template-rows: repeat(2, minmax(100px, auto));

<!-- 지정되지 않은 행 자동 조정 -->
grid-auto-rows: 100px;

```

**2/ 아이템 영역**

```
<!-- 열 3가지 방식 -->
grid-column-start: 2;
grid-column-end: 4;

grid-column: 2/4;

grid-column: 2 / span 2;

<!-- 행 3가지 방식-->
grid-row-start: 1;
grid-row-end: 3;

grid-row: 1/3;

grid-row: 1/ span 2;
```

### 4. 미디어 쿼리를 이용한 적응형 디자인

- **미디어쿼리**
  :미디어에 따른 쿼리: 미디어에 따라 적용될 수 있게 하는 문법
  CSS에서 화면크기, 방향, 해상도, 기기 종류 등에 딸 ㅏ다른 스타일을 적용할 수 있게 해주는 기능

- 적응형 디자인: 특정 해상도에 적응하는 서로다른 코딩을 따로따로 짜겠다는 것. 미디어쿼리 활용
- 반응형 디자인:미디어 쿼리 없이 순수하게 %이용. 특정 해상도 임계점 없이 쭉 통일된 스타일

```
@media [미디어 타입] and( 조건 ) {
    조건에 맞는 스타일
}
/* 미디어타입
- all(기본값), screen(pc/mobile), print(인쇄), speech(음성출력장치) */
/* 조건
- min-width, max-width, min-height, max-height, orientation, resolution*/

```
