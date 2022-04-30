## 1. List

### ul

```html
<!DOCTYPE html>
<html>
  <body>
    <h2>순서없는 목록 (Unordered List)</h2>
    <ul>
      <li>Coffee</li>
      <li>Tea</li>
      <li>Milk</li>
    </ul>
  </body>
</html>
```

<br />

<img style="margin-left:20px;"  width="390" alt="hTag" src="/asset/img/ul.png">

### ol

```html
<!DOCTYPE html>
<html>
  <body>
    <h2>순서있는 목록 (Ordered List)</h2>
    <ol>
      <li>Coffee</li>
      <li>Tea</li>
      <li>Milk</li>
    </ol>
  </body>
</html>
```

<br />

<img style="margin-left:20px;"  width="390" alt="hTag" src="/asset/img/ol.png">

#### ol의 타입

| value | 설명            |
| ----- | --------------- |
| `1`   | 숫자(기본값)    |
| `A`   | 대문자 알패벳   |
| `a`   | 소문자 알패벳   |
| `I`   | 대문자 로마숫자 |
| `i`   | 대문자 로마숫자 |

```html
<ol type="I">
  <li value="2">Coffee</li>
  <li value="4">Tea</li>
  <li>Milk</li>
</ol>
```

<br />

리버스는 순서값을 역으로 표현

```html
<ol reversed>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

<br />

<img style="margin-left:20px;"  width="390" alt="hTag" src="/asset/img/reverseOL.png">

<br />

### 중첩 목록

```html
<!DOCTYPE html>
<html>
  <body>
    <h2>중첩 목록</h2>
    <ul>
      <li>Coffee</li>
      <li>
        Tea
        <ol>
          <li>Black tea</li>
          <li>Green tea</li>
        </ol>
      </li>
      <li>Milk</li>
    </ul>
  </body>
</html>
```

<img style="margin-left:20px;"  width="390" alt="hTag" src="/asset/img/nest.png">

<br />

## 2. Table

표를 만드는 태그

| value   | 설명                              |
| ------- | --------------------------------- |
| `table` | 표를 감싸는 태그                  |
| `tr`    | 표 내부의 행 (table row)          |
| `th`    | 행 내부의 제목 셀 (table heading) |
| `td`    | 행 내부의 일반 셀 (table data)    |

<img style="margin-left:20px;"  width="550" alt="hTag" src="/asset/img/html_table_structure.gif">

```html
<!DOCTYPE html>
<html>
  <body>
    <table border="1">
      <tr>
        <th>First name</th>
        <th>Last name</th>
        <th>Score</th>
      </tr>
      <tr>
        <td>Jill</td>
        <td>Smith</td>
        <td>50</td>
      </tr>
      <tr>
        <td>Eve</td>
        <td>Jackson</td>
        <td>94</td>
      </tr>
      <tr>
        <td>John</td>
        <td>Doe</td>
        <td>80</td>
      </tr>
    </table>
  </body>
</html>
```

<img style="margin-left:20px;"  width="390" alt="hTag" src="/asset/img/table.png">

<br />

테이블 속성

| attribute | 설명                            |
| --------- | ------------------------------- |
| `border`  | 표 테두리 두꼐 지정             |
| `rowspan` | 해당 셀이 점유하는 행의 수 지정 |
| `colspan` | 해딩 셀이 점유하는 열의 수 지정 |

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      table,
      th,
      td {
        border: 1px solid black;
        border-collapse: collapse;
      }
      th,
      td {
        padding: 15px;
      }
    </style>
  </head>
  <body>
    <h2>2개의 culumn을 span</h2>
    <table>
      <tr>
        <th>Name</th>
        <th colspan="2">Telephone</th>
      </tr>
      <tr>
        <td>Bill Gates</td>
        <td>555 77 854</td>
        <td>555 77 855</td>
      </tr>
    </table>

    <h2>2개의 row를 span</h2>
    <table>
      <tr>
        <th>Name:</th>
        <td>Bill Gates</td>
      </tr>
      <tr>
        <th rowspan="2">Telephone:</th>
        <td>555 77 854</td>
      </tr>
      <tr>
        <td>555 77 855</td>
      </tr>
    </table>
  </body>
</html>
```

<img style="margin-left:20px;"  width="400" alt="hTag" src="/asset/img/tableSpan.png">
