# css

## css 세 가지 적용 방식

1. 인라인 (in-line) 적용 방식
    - 속성을 적용할 html 태그에 직접 입력
2. style 태그 이용
    - head 태그 부분에 style 태그를 넣고 그 안에 css를 정의하는 방법
3. 분리된 css 파일 연결
    - html 파일 & css 파일 따로 만든 뒤 link 태그를 이용해서 연결하는 방법

### link 태그

> \<link rel="stylesheet" href="./index.css"\>

- rel: 해당 태그로 연결 시켜줄 파일과 어떤 관계인지 지정
- href: 연결할 파일의 경로를 지정

## 선택자 (Selector)

### tag 선택자: 해당 css가 적용된 모든 태그에 스타일 적용

```css
div {
    background-color: #f9f9f9;
}

h1 {
    font-size: 28px;
    color: red;
}

p {
    color: blue;
}
```

### id 선택자

- 중복 지정할 수 없음

```html
<div id="title">title</div>
```
```css
#title {
    font-size: 28px;
    color: red;
}
```

### class 선택자

- 중복 지정 가능

```html
<div class="title">title1</div>
<div class="title">title2</div>
```
```css
.title {
    font-size: 28px;
    color: red;
}
```

### 자손 선택자

- 특정 태그 안에 포함된 태그를 자식 요소라고 칭함

example
```css
.parent .child {
    property: value;
}
```
```html
<!-- div 태그는 h1 태그와 p 태그의 부모 요소 -->
<div>
    <!-- h1 태그와 p 태그는 div 태그의 자식 요소 -->
    <h1 id="title">제목</h1>
    <p class="contents">내용</p>
</div>
```

#### 특정 자손만 선택하고 싶은 경우

```html
<h1 class="title">전체 제목</h1>
<div class="box1">
    <h1 class="title">제목</h1>
</div>
```
```css
/* box1 클래스 태그의 자식 요소 중 title 클래스를 선택 */
.box1 .title {
    color: red;
}
```

### 다중 선택자

- 여러 선택자를 모두 만족 시키는 태그만 css 영향을 받는다.

```html
<div id="box" class="contents">다중 선택자</div>
```
```css
/* id가 box이고, class에 contents가 포함된 태그에만 적용 */
#box.contents {
    color: red;
}

/* 태그 선택자, id 선택자, class 선택자 모두 혼용해서 사용할 수 있다. */
div#box.contents {
    color: red;
}
```
