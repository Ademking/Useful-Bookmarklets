0) Create a new Bookmarklet in your Bookmarks Bar Using This Code :
```javascript
javascript:void function(){function isElementVisible(el){var rect=el.getBoundingClientRect(),vWidth=window.innerWidth||doc.documentElement.clientWidth,vHeight=window.innerHeight||doc.documentElement.clientHeight,efp=function(x,y){return document.elementFromPoint(x,y)};return rect.right<0||rect.bottom<0||rect.left>vWidth||rect.top>vHeight%3F!1:el.contains(efp(rect.left,rect.top))||el.contains(efp(rect.right,rect.top))||el.contains(efp(rect.right,rect.bottom))||el.contains(efp(rect.left,rect.bottom))}"undefined"==typeof window.isElementVisible;{var imgs=document.querySelectorAll(".irc_mi");imgs.forEach(function(img){isElementVisible(img)%26%26window.open(img.src)})}}();
```
1) Open https://images.google.com and search for any images ... let's say you are looking for "cats"
2) Click on the Image you want to get the Direct URL
2) Run The Bookmarklet
3) Have Fun ♥

###### (*) if you don't know how to make a bookmarket, please follow [this tutorial](https://github.com/Ademking/Useful-Bookmarklets/blob/master/How_To_Create_Bookmarklet.md)
------

### Raw Code : (For Debug)


```javascript
function() {
    function isElementVisible(el) {
        var rect = el.getBoundingClientRect(),
            vWidth = window.innerWidth || doc.documentElement.clientWidth,
            vHeight = window.innerHeight || doc.documentElement.clientHeight,
            efp = function(x, y) {
                return document.elementFromPoint(x, y)
            };
        return rect.right < 0 || rect.bottom < 0 || rect.left > vWidth || rect.top > vHeight % 3 F!1: el.contains(efp(rect.left, rect.top)) || el.contains(efp(rect.right, rect.top)) || el.contains(efp(rect.right, rect.bottom)) || el.contains(efp(rect.left, rect.bottom))
    }
    "undefined" == typeof window.isElementVisible; {
        var imgs = document.querySelectorAll(".irc_mi");
        imgs.forEach(function(img) {
            isElementVisible(img) % 26 % 26 window.open(img.src)
        })
    }
}();

```
