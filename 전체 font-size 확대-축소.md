# 전체 font-size  확대-축소

- HTML
```
<div class="btn">
    <a href="#">확대</a>
    <a href="#">축소</a>
</div>

<h1>hello</h1>
<h2>world</h2>
```

- CSS
```
h1 {
    font-size: 1.5em;
}
h2 {
    font-size: 1.2em;
}
```

- jQuery
```
// 다른 요소의 font-size 단위를 'em'으로 설정하고 body의 font-size만 바꿔주는 예제
$(".btn a").on("click", function () {
    var size = 0;
    var unit = 2; // 확대-축소 단위(px)
    var $body = $("body");
    var bodyFontSize = $body.css("font-size");
    var aIdx = $(this).index();

    switch (aIdx) {
        case 0:
            size = unit;
            break;
        case 1:
            size = -unit;
            break;
    }

    $body.css({
        fontSize: parseInt(bodyFontSize) + size
    });
});
```
