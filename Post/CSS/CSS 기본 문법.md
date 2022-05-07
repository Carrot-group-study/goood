> ## CSS 기본 문법

CSS는 HTML의 각 요소의 style을 정의하여 화면등에 어떻게 렌더링하면 되는지 브라우저에게 설명하기 위한 언어

```css
h1 {
  color: red;
  font-size: 12px;
}
```

- h1이 셀렉터
- color, font-size가 property
- red, 12px이 value

<br />

> ## HTML과 연동하기

<br />

### 1. Link Style

HTML에서 외부 CSS파일을 불러올때 사용한다. 대부분 이 방식을 사용하고 있다.

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="css/style.css" />
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a web page.</p>
  </body>
</html>
```

```css
/* style.css  */
h1 {
  color: red;
}
p {
  background: blue;
}
```

<br />

### 2. Embedding style

`<style></style>`내에 css를 설정

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      h1 {
        color: red;
      }
      p {
        background: aqua;
      }
    </style>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a web page.</p>
  </body>
</html>
```

<br />

### 3. Inline style

HTML요소 안에서 css를 입력

```html
<!DOCTYPE html>
<html>
  <body>
    <h1 style="color: red">Hello World</h1>
    <p style="background: aqua">This is a web page.</p>
  </body>
</html>
```

<br />

> ## CSS초기화 하기

브라우저별로 디폴트 스타일을 하나의 스타일로 맞추기위해 사용하고, CSS 초기화 용도로도 사용

```css
/* http://meyerweb.com/eric/tools/css/reset/
  v2.0 | 20110126
  License: none (public domain)
*/

html,
body,
div,
span,
applet,
object,
iframe,
h1,
h2,
h3,
h4,
h5,
h6,
p,
blockquote,
pre,
a,
abbr,
acronym,
address,
big,
cite,
code,
del,
dfn,
em,
img,
ins,
kbd,
q,
s,
samp,
small,
strike,
strong,
sub,
sup,
tt,
var,
b,
u,
i,
center,
dl,
dt,
dd,
ol,
ul,
li,
fieldset,
form,
label,
legend,
table,
caption,
tbody,
tfoot,
thead,
tr,
th,
td,
article,
aside,
canvas,
details,
embed,
figure,
figcaption,
footer,
header,
hgroup,
menu,
nav,
output,
ruby,
section,
summary,
time,
mark,
audio,
video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
menu,
nav,
section {
  display: block;
}
body {
  line-height: 1;
}
ol,
ul {
  list-style: none;
}
blockquote,
q {
  quotes: none;
}
blockquote:before,
blockquote:after,
q:before,
q:after {
  content: "";
  content: none;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
```

## 참조

- https://poiemaweb.com/css3-syntax
