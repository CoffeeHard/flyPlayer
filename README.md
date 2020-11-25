# flyPlayer

```javascript
<script>
    function makeVideoFly(args) {
        var isMobile = false;
        var isFly = false;
        var bodyWidth = document.querySelector('body').offsetWidth;

        // getting arguments from starter
        var postContainer = document.querySelector(args.postContainer);
        var videoWrap = document.querySelector(args.playerClass);
        var videoWidth = args.playerFixedWidth;
        
        var videoWrapHeight = videoWrap.offsetHeight;
        
        // checking mobile width
        if (bodyWidth < 968) {
            isMobile = true;
        }
        
        // adding class to make videoplayer flying & fixing free space
        function videoFly () {
            if (!isMobile) {
                if (window.pageYOffset > 400) {
                    singlePostOuter.style.paddingTop = videoWrapHeight + 'px';
                    videoWrap.classList.add('video-wrap__fixed');
                } else if (window.pageYOffset <= 400) {
                    singlePostOuter.style.paddingTop = '0px';
                    videoWrap.classList.remove('video-wrap__fixed');
                }
            }
        }
        
        // function starter
        document.addEventListener('scroll', videoFly);
        console.log(postContainer);
        console.log(videoWrap);
        console.log(videoWidth);
    }
</script>
```

## Support
<a href="https://coffeehard.ru/" target="_blank">coffeehard.ru</a>

## License
This project is available under the [MIT](https://opensource.org/licenses/mit-license.php) license.