# 다른 영역 클릭 확인하기
- event.target

````
$(document).on("click", function (e) {
    e.stopPropagation();
    console.log($(e.target).parents().hasClass("ibk_site"));
    if (!$(e.target).parents().hasClass("ibk_site")) {
        $('.ibk_site .body').hide(); // 관련이 있건 없건 모두 닫고 시작!
        $('.ibk_site .head').removeClass('on'); // 관련이 있건 없건 모두 on 클래스 삭제하고 시작!
    }
});
````
