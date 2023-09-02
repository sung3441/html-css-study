# Flex

flex의 속성은 크게 두 가지로 분류할 수 있다.

1. 컨테이너에 적용하는 속성
2. 아이템에 적용하는 속성

## flex 컨테이너에 적용하는 속성들

### display: flex

flex layout을 사용하는 것은 flex 컨테이너에 해당 속성을 적용하는 것으로 시작한다.

```css
.container {
    display: flex;
    /* display: inline-flex */
}
```

다음 속성 적용 시 flex 아이템들은 가로 방향으로 배치되고,
자신이 가진 내용의 width 만큼 영역을 차지한다. 이는 inline 요소의 특징과 같다.

height는 컨테이너의 높이만큼 늘어난다.