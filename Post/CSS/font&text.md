## font-size

- 텍스트의 크기를 정의

```css
.container {
  font-size: 100px;
  /* default font size:16이면 */
  font-size: 2em; /* 32px */
  font-size: 150%; /* 24px */
}
```

<br/>

## font-family

- 폰트를 지정

```css
body {
  font-family: "Times New Roman", Times, serif;
}
```

<br/>

## font-style / font-weight

- `font-style`은 이탤릭체
- `font-weight`는 폰트 굵기 지정

```css
.container {
  font-style: italic;

  /* font-style
      normal / italic / oblique */

  font-weight: 100;
  /* 100 ~ 900 or normal / bold / lighter / bolder */
}
```

<br/>

## line-height

- 텍스트의 높이를 지정

<img style="margin-left:20px;"  width="640" alt="line-height" src="/asset/img/line-height.png">

<br/>

## letter-spacing

- 글자 사이의 간격을 지정

```css
.container {
  letter-spacing: 2px;
}
```

<br/>

## text-align

- 텍스트의 수평 정렬을 정의
- inline요소는 적용되지 않아(width 프로퍼티가 없기 때문) `display:block`으로 설정하면 적용

```css
.container {
  text-align: center;
  /* 텍스트 중앙정렬 */
  /* text-align : 
  left | right | center | justify | inital | inherit 
   왼쪽 | 오른쪽  | 가운데   | 양쪽 정렬 |  기본값 | 부모 요소에서 상속
  */
}
```

<br/>

## text-decoration

- `a`링크 undeline을 제거 할 수 있는 프로퍼티

```css
p {
  text-decoration: underline;
  /* text-decoration 
    none | overline | line-through | underline
     제거 |  위의 줄   |   가운데 줄    |    밑의 줄
  */
}
```

<br />

## white-space

- 공백(space), 들여쓰기(tab), 줄바꿈(line break)을 의미

|  프로퍼티  | line break | space / tab | 자동줄바꿈 |
| :--------: | :--------: | :---------: | :--------: |
|  `normal`  |    무시    | 1번만 반영  |     O      |
|  `nowrap`  |    무시    | 1번만 반영  |     X      |
|   `pre`    |    반영    | 그대로 반영 |     X      |
| `pre-wrap` |    반영    | 그대로 반영 |     O      |
| `pre-line` |    반영    | 1번만 반영  |     O      |

<br/>

## text-overflow

- 부모 영역을 벗어난 wrapping(자동줄바꿈)이 되지 않은 텍스트의 처리 방법을 정의

<br />

조건

- width가 있어야 함, inline이 아닌 block level 요소로 지정해야 한다.
- `white-space : nowrap`로 설정
- overflow에 `visible`외 다른 값이 지정되어야 한다.

```css
.container {
  width: 150px; /* width가 지정되어 있어야 한다. */
  white-space: nowrap; /* 자동 줄바꿈을 방지 */
  overflow: hidden; /* 반드시 "visible" 이외의 값이 지정되어 있어야 한다. */
  text-overflow: ellipsis; /* ellipsis or clip */

  /* clip : 영역 벗어난 부분 표시 하지 않음 |
   ellipsis : 영역 벗어난 부분 잘래내고 말줄임표 표시 */
}
```

## 참조

https://poiemaweb.com/css3-font-text
