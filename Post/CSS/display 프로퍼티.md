## display 프로퍼티

| 프로퍼티       | 설명                              |
| -------------- | --------------------------------- |
| `block`        | block 레벨 요소 지정              |
| `inline`       | inline 레벨 요소 지정             |
| `inline-block` | inline-block 레벨 요소 지정       |
| `none`         | 해당 요소를 화면에 표시 하지 않음 |

### block 레벨 요소

- width, height, margin, padding 프로퍼티 지정이 가능
- 화면 크기 전체의 가로폭을 차지
- 항상 새로운 라인
- `div, h1~h6, p, ol, ul, li, hr, table, form`

```html
<head>
  <style>
    div {
      color: white;
    }
    div:nth-of-type(1) {
      background-color: #ffa07a;
      padding: 20px;
      width: 300px;
    }
    div:nth-of-type(2) {
      background-color: #ff7f50;
      padding: 20px;
      width: 300px;
    }
    div:nth-of-type(3) {
      background-color: #c24213;
      padding: 20px;
      width: 300px;
    }
  </style>
</head>
<body>
  <div>
    <h2>블록 레벨 요소</h2>
  </div>
  <div>
    <h2>블록 레벨 요소</h2>
  </div>
  <div>
    <h2>블록 레벨 요소</h2>
  </div>
</body>
```

<img style="margin-left:20px;"  width="360" alt="blockLevel" src="/asset/img/blockLevel.png">

<br />

### inline 레벨 요소

- 새로운 라인이 아니라 옆에 요소를 한 행에 추가 할 수 있음.
- width, height, margin-top, margin-bottom 프로퍼티 지정할 수 없고 상 하 여백은 line-height로 지정
- `span, a, strong, img, br, input, select, textarea, button`

```html
<head>
  <style>
    span {
      background-color: red;
      color: white;
    }
  </style>
</head>
<body>
  <h1>My <span>Important</span> Heading</h1>
  <span>Inline</span>
  <span>Inline</span><span>Inline</span>
</body>
```

<img style="margin-left:20px;"  width="340" alt="inlineLevel" src="/asset/img/inlineLevel.png">

<br />

### inline과 block 비교

```html
<head>
  <style>
    .test1 {
      background-color: red;
      display: inline;
    }
    .test2 {
      background-color: yellow;
      display: inline;
    }
    .test3 {
      background-color: orange;
      display: block;
    }
  </style>
</head>
<body>
  <div class="test1">Test1</div>
  <div class="test2">Test2</div>
  <div class="test3">Test3</div>
</body>
```

<img style="margin-left:20px;"  width="1000" alt="inline&block" src="/asset/img/inline&block.png">

<br />

### inline-block

- block과 inline의 특징을 가지고 있음.
- 줄을 바꾸지 않고 한줄에 표시되고, width, height, margin, padding를 모두 지정할 수 있음

```html
<head>
  <style>
    span {
      display: inline-block;
      width: 100px;
      background-color: yellow;
      text-align: center;
    }
  </style>
</head>
<body>
  before
  <a>A</a>
  <span>SPAN</span>
  <!-- inline 요소이지만, inline-block으로 선언했기 때문에 width가 적용 됨 -->
  <em>EM</em>
  after
</body>
```

<img style="margin-left:20px;"  width="340" alt="inline-block" src="/asset/img/inline-block.png">

<br />

## visibility 프로퍼티

| 속성     | 설명                                             |
| -------- | ------------------------------------------------ |
| visible  | 해당 요소 보임                                   |
| hidden   | 해당 요소 보이지 않게 함                         |
| collapse | table 요소에 사용하며 행이나 열을 보이지 않게 함 |
| none     | table 요소 row colummn을 보이지 않게 한다.       |

### display:none과 visibility:hidden 차이점

```html
<head>
  <style>
    .test1 {
      background-color: red;
      width: 100px;
      height: 100px;
      display: inline-block;
    }
    .test2 {
      background-color: green;
      width: 100px;
      height: 100px;
      display: inline-block;
      visibility: hidden;
    }
    .test3 {
      background-color: yellow;
      width: 100px;
      height: 100px;
      display: inline-block;
    }
  </style>
</head>
<body>
  <div class="test1"></div>
  <div class="test2"></div>
  <div class="test3"></div>
</body>
```

<img style="margin-left:20px;"  width="330" alt="visibility-hiden" src="/asset/img/visibility-hiden.png">

<br />

```html
<head>
  <style>
    .test1 {
      display: inline-block;
      background-color: red;
      width: 100px;
      height: 100px;
    }
    .test2 {
      background-color: green;
      width: 100px;
      height: 100px;
      display: none;
    }
    .test3 {
      background-color: yellow;
      width: 100px;
      height: 100px;
      display: inline-block;
    }
  </style>
</head>
<body>
  <div class="test1"></div>
  <div class="test2"></div>
  <div class="test3"></div>
</body>
```

<img style="margin-left:20px;"  width="220" alt="display-none" src="/asset/img/display-none.png">

<br />

## opacity 프로퍼티

- 투명도 설정 0.0 ~ 1.0사이의 값 값이 높을 수록 불투명해짐

```html
<head>
  <style>
    .test1 {
      background-color: red;
      width: 100px;
      height: 100px;
      opacity: 1;
    }
    .test2 {
      background-color: red;
      width: 100px;
      height: 100px;
      opacity: 0.5;
    }
    .test3 {
      background-color: red;
      width: 100px;
      height: 100px;
      opacity: 0.2;
    }
  </style>
</head>
<body>
  <div class="test1"></div>
  <div class="test2"></div>
  <div class="test3"></div>
</body>
```

<img style="margin-left:20px;"  width="120" alt="opacity" src="/asset/img/opacity.png">

## 참조

https://poiemaweb.com/css3-display
