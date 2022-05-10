## 박스 모델

- 박스 모델에서 contents, padding, Border, Margin으로 구성

크롬 개발자 도구의 박스모델 <br />
<img style="margin-left:20px;"  width="300" alt="boxmodel" src="/asset/img/boxmodel.png">

<br />

| Box Model | 설명                               |
| --------- | ---------------------------------- |
| Content   | 실제 내용이 위치하는 부분          |
| Padding   | Border 안쪽 부분 여백 영역(내부)   |
| Border    | 테두리 영역                        |
| Margin    | Border 바깥쪽 부분 여백 영역(외부) |

<br />

4개의 박스모델은 4방향을 설정 할 수 있다.

- top, right, bottom, left

4개의 값을 지정할 때

```css
.four {
  margin: 25px 50px 75px 100px;

  margin-top: 25px;
  margin-right: 50px;
  margin-bottom: 75px;
  margin-left: 100px;
}
```

3개의 값을 지정할 때

```css
.three {
  margin: 25px 50px 75px;

  margin-top: 25px;
  margin-right: 50px margin-left: 50px;
  margin-bottom: 75px;
}
```

2개의 값을 지정할 때

```css
.two {
  margin: 25px 50px;

  margin-top: 25px margin-bottom: 25px;
  margin-right: 50px margin-left: 50px;
}
```

1개의 값을 지정할 때

```css
.one{
margin: 25px;
margin-top: 25px margin-right: 25px margin-bottom: 25px margin-left: 25px;
}
```

> ## max-width
>
> max-width CSS 속성은 요소의 최대 너비를 설정합니다. <br />
> max-width는 width 속성의 사용값이 자신의 값보다 커지는걸 방지합니다.

> ## min-width
>
> min-width CSS 속성은 요소의 최소 너비를 설정합니다. <br />
> min-width는 width 속성의 사용값이 자신의 값보다 작아지는걸 방지합니다.

<br />

## box-sizing 프로퍼티

```css
div {
  box-sizing: content-box; /* default, content안의 width,height값을 의미 */
  box-sizing: border-box; /* content + padding + border가 포함된 값 */
}
```

<br />

<img style="margin-left:20px;"  width="558" alt="box-sizing" src="/asset/img/box-sizing.png">

```css
.content-box {
  box-sizing: content-box;
  width: 600px; /* content 영역의 width 600px */
  border: 10px;
  padding: 50px;
  margin: 50px;
}

.border-box {
  box-sizing: border-box;
  width: 600px; /* content 영역의 width 480px */
  border: 10px;
  padding: 50px;
  margin: 50px;
}
```

- content-box에서 content의 width 600px
- border-box에서 content의 width는 왼쪽 오른쪽 border와 padding값을 뺀 값이므로 600px - (10px \* 2) - (50px \* 2) = 480px

## 참조

https://poiemaweb.com/css3-box-model
