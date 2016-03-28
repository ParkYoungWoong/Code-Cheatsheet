# event object로 요소 기준 위치 알아내기
- event.pageX가 document를 기준으로 하기 때문에 요소를 기준으로 위치 값을 알아내려면 다음과 같이 작성

```
$('element').on('mousemove', function (e) {
  var x = e.pageX - $(this).offset().left,
      y = e.pageY - $(this).offset().top;
  console.log(x, y);
});
```
