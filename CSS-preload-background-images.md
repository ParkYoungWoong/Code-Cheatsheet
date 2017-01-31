# CSS preload background images

CSS 에서 사용하는 images 들을 미리 로드하여 호출 시 중간 호출 시 끊김현상이 발생하지 않도록 한다.

```css
body::after {
    content:"";
    width: 0;
    height: 0;
    background:
        url("../img/menu_nav1.png"),
        url("../img/menu_nav2.png"),
        url("../img/menu_nav3.png"),
        url("../img/menu_nav4.png"),
        url("../img/menu_nav1_on.png"),
        url("../img/menu_nav2_on.png"),
        url("../img/menu_nav3_on.png"),
        url("../img/menu_nav4_on.png")
}
```
