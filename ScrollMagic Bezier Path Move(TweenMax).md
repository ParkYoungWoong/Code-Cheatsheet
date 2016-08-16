# ScrollMagic Bezier Path Move

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/1.16.0/TweenMax.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/ScrollMagic/2.0.3/ScrollMagic.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/ScrollMagic/2.0.3/plugins/animation.gsap.min.js"></script>
```

```js
var aniPath = {
        route : {
            curviness: 0.8,
            autoRotate: false,
            values: [
                {top: 604, left: 1245},
                {top: 1056, left: 1451},
                {top: 1725, left: 1314},
                {top: 2333, left: 426},
                {top: 3073, left: 1286},
                {top: 3963, left: 729}
            ]
        }
    };


    var controller = new ScrollMagic.Controller();

    var tween = new TimelineMax();
    tween.to($moveBee, 20, {css:{bezier:aniPath.route}, ease:Power1.easeInOut});

    var scene = new ScrollMagic.Scene({
        triggerElement: $('.sec1')[0],
        triggerHook: "onLeave",
        duration: 4000,
        offset: 0
    })
        .setTween(tween)
        .addTo(controller);
```
