# Mobile Check Redirection
- 모바일 디바이스를 체크하여 모바일페이지로 리다이렉션하는 코드

### 운영체제로 체크
~~~~
var filter = "win16|win32|win64|mac";
if( navigator.platform ){
    if( filter.indexOf(navigator.platform.toLowerCase()) < 0 ){
        location.href = "http://www.naver.com"
    }
}
~~~~

### 디바이스 기종으로 체크
~~~~
if( navigator.userAgent.match(/Android/i)
    || navigator.userAgent.match(/webOS/i)
    || navigator.userAgent.match(/iPhone/i)
    || navigator.userAgent.match(/iPad/i)
    || navigator.userAgent.match(/iPod/i)
    || navigator.userAgent.match(/BlackBerry/i)
    || navigator.userAgent.match(/Windows Phone/i)
){
    location.href = "http://herop.me/mobile"
}
~~~~
