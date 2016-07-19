# setInterval() 을 setTiemout() 으로 대체하기
- setInterval() 은 시스템의 환경에 영향을 받기 때문에 정확하지 않을 수 있음

````js
var timer = null;
function myTimeOutFunc() {
    var d = new Date();
    var year = d.getFullYear();
    var month = d.getMonth() + 1;
    var day = d.getDate();
    var hour = d.getHours();
    var min = d.getMinutes();
    var sec = d.getSeconds();

    console.log(year, month, day, hour, min, sec);
    timer = setTimeout(myTimeOutFunc, 1000);
}
myTimeOutFunc();

$(function () {
    $(".end").on("click", function () {
        console.log("end");
        clearTimeout(timer);
    });
});
````
