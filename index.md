# Mobile Swipe Menu
### Example
#### ES6
```javascript
import MobileSwipeMenu from 'mobile-swipe-menu';
new MobileSwipeMenu('#menu', {
    mode: 'right',
    width: window.innerWidth / 1.15
});
```
#### OR
```html
<script src="js/mobile-swipe-menu.min.js"></script>
<script>
    var mobileMenu = new MobileSwipeMenu('#menu', {
        mode: 'right',
        width: window.innerWidth / 1.15,
        hookWidth: 15,
        events: {
            opening: function () {
                console.log(this, 'Opened');
            },
            closing: function () {
                console.log(this, 'Closed');
            },
            drag: function (swipe) {
                console.log(this, swipe);
            }
        }
    });
    document.getElementById('openMenu').addEventListener('click', function () {
        mobileMenu.open();
    });
    document.getElementById('closeMenu').addEventListener('click', function () {
        mobileMenu.close();
    });
    document.getElementById('toggleMenu').addEventListener('click', function () {
        mobileMenu.toggle();
    });
</script>
```