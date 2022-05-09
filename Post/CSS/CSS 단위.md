## 크기 단위

- 대부분 브라우저 폰트 사이즈 단위는 16px, 1rem, 100%이다.
- px은 절대값, em, %등은 상대값

<br />

### px

px은 픽셀 단위, 1px은 화소 1개 크기, 절대 단위

```css
font-size: 16px;
```

<br />

### %

백분율 단위, 요소에 지정된 사이즈에 상대적 사이즈 결정

```html
<style>
  body {
    font-size: 14px;
  }
  div {
    font-size: 120%;
    /* 14 * 1.2 = 16.8px */
    padding: 2em;
    /* 16.8px * 2 = 33.6px */
  }
</style>
<body>
  <div>Font size: 14px * 120% → 16.8px</div>
</body>
```

<br />

### em

요소에 지정된 폰트 사이즈에 상대적인 사이즈를 설정

```html
<style>
  body {
    font-size: 14px;
    text-align: center;
  }
  div {
    font-size: 1.2em; /* 14px * 1.2 = 16.8px */
    font-weight: bold;
    padding: 2em; /* 16.8px * 2 = 33.6px */
  }
</style>

<body>
  <div>Font size: 1.2em → 14px * 1.2 = 16.8px</div>
</body>
```

중첩된 자식들에게`em`을 선언하면 자식의 사이즈에 영향을 미처서 `em`대신 `rem`을 사용해야 한다.

```html
  <style>
    body {
      font-size: 14px;
      text-align: center;
    }
    div {
      font-size: 1.2em; /* 14px * 1.2 = 16.8px */
      font-weight: bold;
      padding: 2em;
    }
  </style>
</head>
<body>
  <div class='box1'>
    Font size: 1.2em ⇒ 14px * 1.2 = 16.8px
    <div class='box2'>
      Font size: 1.2em ⇒ 16.8px * 1.2 = 20.16px
      <div class='box3'>
        Font size: 1.2em ⇒ 20.16px * 1.2 = 24.192px
      </div>
    </div>
  </div>
</body>
```

<br />

### rem

- em은 상속에 따라 변경 된다. rem은 최상위 요소(html)의 폰트 사이즈에 기준을 잡음
- html에 font-size를 지정하지 않으면 디폴트값으로 16px로 지정된다.

```html
<html>
  <style>
    html {
      font-size: 14px;
      text-align: center;
    }
    div {
      font-size: 1.2rem; /* 14px * 1.2 = 16.8px */
      font-weight: bold;
      padding: 2em; /* 16.8px * 2 = 33.6px */
    }
  </style>
</head>
<body>
  <div class='box1'>
    Font size: 1.2rem ⇒ 14px * 1.2 = 16.8px
    <div class='box2'>
      Font size: 1.2rem ⇒ 14px * 1.2 = 16.8px
      <div class='box3'>
        Font size: 1.2rem ⇒ 14px * 1.2 = 16.8px
      </div>
    </div>
  </div>
</body>
</html>
```

<br />

### viewport

- viewport : 브라우저에서 웹페이지를 사용자에게 보여지는 부분
- 반응형 웹 화면 크기의 동적으로 대응하기 위해 사용

<br />

| 단위   | 설명                                       |
| ------ | ------------------------------------------ |
| `vw`   | viewport 너비의 1/100                      |
| `vh`   | viewport 높이의 1/100                      |
| `vmin` | viewport 너비 또는 높이 중 작은 쪽의 1/100 |
| `vmax` | viewport 너비 또는 높이 중 큰 쪽의 1/100   |

<br />

viewport 너비가 1000px 높이가 600px이면

- `1vw` : viewport 너비 1000px에서 1%인 10px
- `1vh` : viewport 높이 600px에서 1%인 6px
- `vmin` : viewport 너비보다 높이가 작기 떄문에 높이 사이즈 기준인 600px에서 1%인 6px
- `vmax` : viewport 높이보다 너비가 크기 떄문에 너비 사이즈 기준인 1000px에서 1%인 10px

<br />

## CSS 색상 단위

| 단위                                            | 예                     |
| ----------------------------------------------- | ---------------------- |
| HEX(Hexadecimal Colors)                         | #000000                |
| RGB(Red, Green, Blue)                           | rgb(255,255,0)         |
| RGBA (Red, Green, Blue, Alpha/투명도)           | rgba(255,255,0,1)      |
| HSL (Hue/색상, Saturation/채도, Lightness/명도) | hsl(0, 100%, 25%)      |
| HSLA (Hue, Saturation, Lightness, Alpha)        | hsla(60, 100%, 50%, 1) |

## 참조

https://poiemaweb.com/css3-units
