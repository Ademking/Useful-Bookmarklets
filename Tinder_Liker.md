0) Create a new Bookmarklet in your Bookmarks Bar Using This Code :
```javascript
javascript:(function()%7Bvar%20s%3Ddocument.createElement('script')%3Bs.setAttribute('src'%2C'https%3A%2F%2Fcode.jquery.com%2Fjquery.js')%3Bdocument.getElementsByTagName('body')%5B0%5D.appendChild(s)%3Bwindow.setInterval(function()%7B%24(%22.recsGamepad__button--like%22).click()%7D%2C%202000)%7D)()```
1) Open https://tinder.com and Log In
2) Run The Bookmarklet
3) Have Fun ♥

###### (*) if you don't know how to make a bookmarket, please follow this tutorial
------

### Raw Code : (For Debug)


```javascript
var s=document.createElement('script');
s.setAttribute('src','https://code.jquery.com/jquery.js');
document.getElementsByTagName('body')[0].appendChild(s);

window.setInterval(function(){
	$(".recsGamepad__button--like").click()
}, 2000);

```
