## Hyperlink

- 한 텍스트에서 다른 텍스트 건너뛰 읽을 수 있는 기능
- HTML link는 hyperlink를 의미하고, a tag가 그 역할을 함

### 1 href 어트리뷰트

이동하고자 하는 파일의 위치(경로)를 값으로 받음

#### 1.1 디렉터리(Directory)

- ./ 작업중인 현재 디렉터리
- ../ 현재에서 상위 디렉터리

#### 1.2 파일 경로(File path)

- 절대 경로 : 루트 디렉터리를 기준으로 파일 위치 나타냄 `/Users/goood/Desktop/index.html`, `/index.html`, `http://mysite.com/index.html`
- 상대 경로 : 현재 작업 디렉터리 기준으로 특정 파일의 위치를 나타냄 `./index.html`, `../dist/index.js`, `html/index.html`

```html
<!DOCTYPE html>
<html>
  <body>
    <a href="http://www.google.com">URL</a><br />
    <!-- 절대 URL -->
    <a href="html/my.html">Local file</a><br />
    <!-- 상대 URL -->
    <a href="file/my.pdf" download>Download file</a><br />
    <!-- 상대 경로 파일 -->
    <a href="#">fragment identifier</a><br />
    <!-- 페이지내의 특정 id를 갖는 요소에서의 링크 -->
    <a href="mailto:someone@example.com?Subject=Hello again">Send Mail</a><br />
    <!-- 메일 -->
    <a href="javascript:alert('Hello');">Javascript</a>
    <!-- 자바스크립트 -->
  </body>
</html>
```

### 2. target 어트리뷰트

| value    | 설명                                         |
| -------- | -------------------------------------------- |
| `_self`  | 링크를 클릭 할 경우 현재 윈도우에 열림       |
| `_blank` | 링크를 클릭 하면 새로운 윈도우나 탭에서 열림 |
