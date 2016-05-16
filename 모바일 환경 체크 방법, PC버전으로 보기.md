# 모바일 환경 체크 리다이렉션

### 운영체제로 체크
~~~~
var filter = "win16|win32|win64|mac";
if( navigator.platform ) {
    if( filter.indexOf(navigator.platform.toLowerCase()) < 0 ){
        // Redirection할 페이지 URL
        location.href = "http://www.naver.com";
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
) {
    // Redirection할 페이지 URL
    location.href = "http://www.naver.com";
}
~~~~

# 'PC버전 보기'를 위한 조건문

#### 고정형 사이트의 최상단에 삽입
~~~~
if (location.href.indexOf("desktopMode") === -1) {
    // 모바일 환경 체크 리다이렉션 코드 삽입
}
~~~~

#### 'PC버전 보기' 버튼 URL
~~~~
<a href="http://www.naver.com?desktopMode">DESKTOP MODE</a>
~~~~
