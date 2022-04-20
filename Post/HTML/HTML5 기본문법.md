# 1. HTML5

- HTML은 (Hyper Text Markup Languege)의 약자
- 웹페이지의 내용과 구조를 담당
- 기능 추가
  - 어느 플러그인 설치 없이 비디오 및 오디오 재생을 자체적으로 지원 `<audio>`, `<embed>`, `<source>`, `<track>`, `<video>`
  - 그래픽 및 SVG을 지원 `<svg>`, `<canvas>`
  - 서버와 소켓 통신 지원, 양방향 통신이 가능해짐
  - 카메라 및 동작 센서 등 하드웨어 직접 제어 가능
  - 오프라인 상태에서도 어플리케이션 동작 가능
  - 시멘텍 태그를 도입하여 태그를 명확하게 구별가능해짐
  - CSS3를 완벽히 지원

# 2. Hello HTML5

- HTML5를 사용하려면 첫번째 라인에 `<!DOCTYPE html>` 를 선언한다.
- `<html></html>` 안에 실질적 tag를 기술한다.

```html
<!DOCTYPE html>
<html>
  <head>
    title, 외부 파일 참조, 메타데이터 등이 들어오고, 브라우저에는 표시되지 않음
  </head>
  <body>
    실질적 웹브라우저에 표시 되는 부분
  </body>
</html>
```

## 예문

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <!-- charset 속성으로 명시한 문자 인코딩 방식을 재정의, 여기서는 유니코드 문자셋으로 선언함 -->
    <title>Hello World</title>
    <!-- 브라우저 상단 탭에 표시되는 텍스트 -->
  </head>
  ...
</html>
```

# 3. HTML5의 기본 문법

## 요소

<img style="margin-left:20px;"  width="500" alt="numberWord" src="/asset/img/htmlElement.png">

```
여는 태그 : <p>
어트리뷰트 : class = "nice"
content : Hello world
닫는 태그 : </p>
```

## 어트리뷰트

- 요소의 성질, 특징을 정의하는 명세
- 위의 그림에서 `class`가 어트리뷰트명이되고 `nice`가 어트리뷰트 값이 된다.

## 주석

- html내에 코드를 설명하기 위해 사용되고, html태그내에 영향을 주지 않는다.

# 참조

- https://poiemaweb.com/html5-syntax
- https://developer.mozilla.org/ko/docs/Glossary/Element
