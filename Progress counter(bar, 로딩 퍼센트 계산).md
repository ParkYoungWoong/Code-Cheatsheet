# Progress Counter(bar) 계산하기

웹사이트 최초 로딩 등에서 사용할 수 있는 카운터 계산 JavaScript.  

JavaScript `complete` Property 를 활용하여 웹사이트의 모든 이미지 로딩을 계산함.

```js
document.imageObject.complete
// return Boolean
```

```js
var progressCounter = setInterval(function () {
    if (document.images.length === 0) return false;

    var loaded = 0;
    for (var i = 0; i < document.images.length; i++) {
        if (document.images[i].complete) loaded++;
    }

    var percentage = Math.round(100 * loaded / document.images.length);
    document.getElementById("progress").innerHTML = percentage + "%";

    if (percentage == 100) clearInterval(progressCounter);
}, 10);
```
