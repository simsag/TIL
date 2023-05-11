# CSS 기본 문법

CSS는 문서를 화면, 종이 등에 어떻게 렌더링할 것인지를 위한 언어 

## 1. 셀렉터 (Selector, 선택자)
셀렉터는 스타일을 적용하고자 하는 HTML 요소를 선택하기 위해 CSS에서 제공하는 수단
![images](https://poiemaweb.com/img/css-syntax.png)

- 위의 CSS Rule set은 HTML 문서에 속해 있는 셀렉터를 통해 모든 h1 요소를 선택한 후 선택된 h1 요소의 스타일을 선언 블록에서 정의하고 있다
.

- 이와 같은 Rule Set의 집합을 스타일시트(Style Sheet)라 한다.

## 2. 프로퍼티 (Property / 속성)
프로퍼티는 표준 스펙으로 이미 지정되어 있는 것을 사용하여야하며 사용자가 임의로 정의 할 수 없다. 여러 개의 프로퍼티를 연속해서 지정할 수 있으며 세미콜론(;)으로 구분한다.

```css
p {
  color: ...;
  font-size: ...;
}
```

## 3. 값 (Value / 속성값)
프로퍼티의 값은 해당 프로퍼티에 사용할 수 있는 값을 “키워드”나 “크기 단위” 또는 “색상 표현 단위” 등의 특정 단위로 지정하여야 한다.
```css
p {
  color: orange;
  font-size: 16px;
}
```

## 4. HTML과 CSS의 연동
CSS를 가지고 있지 않은 HTML은 브라우저에서 기본으로 적용하는 CSS(user agent stylesheet)에 의해 렌더링

### 4-1 Link style
HTML에서 외부에 있는 CSS 파일을 로드하는 방식, 가장 일반적으로 사용

```css
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="css/style.css">
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a web page.</p>
  </body>
</html>
```

### 4-2 Embedding style
위와 다르게 HTML 내부에 CSS를 포함시키는 방식, 하지만 HTML과 CSS는 서로 역할이 다르므로 다른 파일로 구분되어 작성하고 관리되는 것이 바람직
```css
<!DOCTYPE html>
<html>
  <head>
    <style>
      h1 { color: red; }
      p  { background: aqua; }
    </style>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a web page.</p>
  </body>
</html>
```
### 4-3 Inline style
HTML요소의 style 프로퍼티에 CSS를 기술하는 방식, JavaScript가 동적으로 CSS를 생성할 때 사용하는 경우
```css
<!DOCTYPE html>
<html>
  <body>
    <h1 style="color: red">Hello World</h1>
    <p style="background: aqua">This is a web page.</p>
  </body>
</html>
```

## 5. Reset CSS 사용하기
- 모든 웹 브라우저는 디폴트 스타일(브라우저가 내장하고 있는 기본 스타일)을 가지고 있어 CSS가 없어도 작동, 하지만 웹브라우저에 따라 디폴트 상이하고 지원하는 tag나 style도 제각각이어서 주의가 필요**
- eset CSS는 기본적인 HTML 요소의 CSS를 초기화하는 용도로 사용, 즉, 브라우저 별로 제각각인 디폴트 스타일을 하나의 스타일로 통일시켜 주는 역할
```css
/* http://meyerweb.com/eric/tools/css/reset/
  v2.0 | 20110126
  License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed,
figure, figcaption, footer, header, hgroup,
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure,
footer, header, hgroup, menu, nav, section {
  display: block;
}
body {
  line-height: 1;
}
ol, ul {
  list-style: none;
}
blockquote, q {
  quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
  content: '';
  content: none;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
```
