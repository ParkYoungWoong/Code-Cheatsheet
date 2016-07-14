# 그림자 출력시 스크롤 막기
- `touchmove`와 `mousewheel`의 기본이벤트 제거하고 버블링 정지

```js
$('.dimming').on('touchmove mousewheel', function (e) {
  e.preventDefault();
  e.stopPropagation();
});
```
