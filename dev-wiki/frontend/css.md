# CSS

### **CSS 개념**

**CSS는 'Cascading Style Sheets'의 약자이다.**

**CSS를 사용하여 브라우저에서 HTML 요소의 모양을 제어하고 원하는 디자인으로 변경할 수 있다.**

### **CSS 구조**

**기본적으로 CSS는 선택자 {속성 : 값;} 의 형태로 이루어져 있다.**

> 💡예시 \
> div { color : red; }
>
> .btn {\
> color : blue;\
> margin-left : 30px;          \
> }

### **CSS 선언 방식**

**내장방식**

태그의 내용으로 스타일을 작성하는 방식이다.

```
<!DOCTYPE html>
<html lang="ko">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
        <!-- 스타일 태그 안에 내용 입력 -->
        <style>
            body {
                font-size: 24px;
                width: auto;
                height: auto;
            }
        </style>
    </head>
    <body>
    </body>
</html>
```

**링크방식**

html 파일 헤더 부분에 css파일 링크를 연결하여 사용하는 방식이다.

```
<!DOCTYPE html>
<html lang="ko">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
        <!-- html 과 css 연결 -->
        <link rel="stylesheet" href="./main.css">
    </head>
    <body>
    </body>
</html>
```

**import 방식**

&#x20;CSS문서 안에서 또 다른 CSS문서를 가져와 연결하는 방식이다.

```
/*가져올 css파일*/
@import url("./main.css");

/*현재 문서 내용*/
div {
    margin: auto;
}
```

**인라인 방식**

요소의 style속성에 직접 스타일을 작성하는 방식이다.

```
<!DOCTYPE html>
<html lang="ko">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        <!-- 태그안에 스타일 속성으로 적용 -->
        <div class="header" style="width: 1100px;"></div>
    </body>
</html>
```

### **CSS 선택자**

**기본선택자**

```
*{} /*전체 선택자*/

div{} /*태그선택자*/

.examlple{} /*클래스 선택자*/

#examlple{} /*id선택자*/
```

**복합 선택자**

```
/*클래스명 : examlple*/

div.example{} /*일치 선택자*/

ul > .examlple{}  /*자식 선택자*/

div .examlple{} /*하위(후손) 선택자*/

.examlple + li{} /*인접 형제 선택자*/

.examlple ~ li{} /*일반 형제 선택자*/
```

**가상 클래스 선택자**

```
div:hover{} /*요소가 마우스커서에 올라가 있는 동안 선택*/

div:active{} /*요소에 마우스를 클릭하고 있는 동안 선택*/

input:focus{} /*요소가 포커스되면 선택(INPUT,A,BUTTON,LABEL,SELECT...)*/

.exmaple span:first-child{}  /*선택자가 형제 요소 중 첫째 선택*/

.exmaple span:last-child{}` /*선택자가 형제 요소 중 막내 선택*/

.exmaple *:nth-child(n){}` /*선택자가 형제 요소 중 (n)번째라면 선택*/

.exmaple *:not(span){} /*선택자가 아닌 요소 선택*/
```

**가상 요소 선택자**

```
.exmaple::before{ content : ""; } /*선택자 요소의 내부 앞에 내용을 삽입*/

.exmaple::after{ content : ""; }  /*선택자 요소의 내부 뒤에 내용을 삽입*/
```

**속성 선택자**

```
[html속성]{}  /*속성을 포함한 요소 선택*/

[속성= "속성값"]{} /*속성을 포함하고 속성값이 일치하는 요소 선택*/
```
