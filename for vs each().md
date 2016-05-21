# JavaScript for문과 jQuery each() 차이점
- JS 코드 참고

### HTML
````
<ul class="each">
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ul>

<ul class="for">
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ul>
````

### CSS
````
ul {
    position: relative;
    width: 300px;
    height: 300px;
    float: left;
    margin-right: 20px;
}
li {
    width: 100px;
    height: 100px;
    position: absolute;
    background-color: red;
}
````

### JS
````
$(function () {
    var colorArray = ['red', 'orange', 'yellow', 'green', 'blue', 'indigo', 'violet', 'white', 'black'];

    eachMethod($('.each li'), colorArray);
    forStatements($('.for li'), colorArray, $('.for li').length );
});

function eachMethod(ele, color) {
    ele.each(function (i) {
        var left = (i % 3) * 100, // [0, 1, 2, 0, 1, 2, 0, 1, 2]
            top = parseInt(i / 3) * 100; // [0, 0, 0, 1, 1, 1, 2, 2, 2]
        ele.eq(i)
            .css({
                left: left
                , top: top
                , backgroundColor: color[i]
            })
            .text(i);
    });
}

function forStatements(ele, color, length) {
    for (var i = 0; i < length; i++) {
        var left = (i % 3) * 100, // [0, 1, 2, 0, 1, 2, 0, 1, 2]
            top = parseInt(i / 3) * 100; // [0, 0, 0, 1, 1, 1, 2, 2, 2]
        ele.eq(i)
            .css({
                left: left
                , top: top
                , backgroundColor: color[i]
            })
            .text(i);
    }
}
````

