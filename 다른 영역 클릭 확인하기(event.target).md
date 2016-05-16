# 다른 영역 클릭 확인하기
- event.target

````
$("*", document.body).on("click", function (e) {
    e.stopPropagation();
    if (!$(e.target).parents().hasClass("클래스이름")) {
        // 다른 영역을 클릭했을 때의 동작
    }
});
````
