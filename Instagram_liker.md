###### 0. Create a new Bookmarklet in your Bookmarks Bar (*)
###### 1. Open Your Instagram Account
###### 2. Choose a Hashtag : example => Cats
###### 3. Replace this with your hashtag : 
###### https://www.instagram.com/explore/tags/{{hashtag}}
###### Example : https://www.instagram.com/explore/tags/cats
###### 4. Open The First Picture
###### 5. Run The Bookmarklet
###### 6. Have Fun ♥

###### (*) if you don't know how to make a bookmarket, please follow this tutorial

```javascript
javascript:(function()%7Bvar%20s%3Ddocument.createElement('script')%3Bs.setAttribute('src'%2C'https%3A%2F%2Fcode.jquery.com%2Fjquery.js')%3Bdocument.getElementsByTagName('body')%5B0%5D.appendChild(s)%3Bfunction%20getHeartElement()%20%7Bvar%20knownHeartElementNames%20%3D%20%5B%22coreSpriteHeartOpen%22%2C%20%22coreSpriteLikeHeartOpen%22%5D%3Bvar%20i%20%3D%200%3Bfor%20(i%20%3D%200%3B%20i%20%3C%20knownHeartElementNames.length%3B%20i%2B%2B)%20%7Bvar%20heartElement%20%3D%20document.querySelector('.'%20%2B%20knownHeartElementNames%5Bi%5D)%3Bif%20(heartElement%20!%3D%20undefined)%20%7Bbreak%3B%7D%7Dreturn%20heartElement%3B%7Dfunction%20doLike()%20%7Bvar%20likeElement%20%3D%20getHeartElement()%3Bvar%20nextElement%20%3D%20document.querySelector('.coreSpriteRightPaginationArrow')%3BlikeCount%2B%2B%3Bconsole.log('Liked%20'%20%2B%20likeCount)%3Bvar%20nextTime%20%3D%20(Math.random()%20*%205000)%20%2B%201000%3Bvar%20FollowButton%20%3D%20document.querySelector('._qv64e')%3BFollowButton.click()%3Bif%20(%20getHeartElement()%20!%3D%20null)%20%7BlikeElement.click()%3B%7DsetTimeout(function()%20%7BnextElement.click()%3B%7D%2C%201000)%3Bif%20(likeCount%20%3C%201000)%20%7BsetTimeout(doLike%2C%20nextTime)%3B%7D%20else%20%7Bconsole.log('Nice!%20Time%20for%20a%20break.')%3B%7D%7Dvar%20likeCount%20%3D%200%3BdoLike()%7D)()
```



### Raw Code : (For Debug)


```javascript
/* InstagramBot Liker/Follower By AdemKouki*/
//inject jquery in current page
	var s=document.createElement('script');
	s.setAttribute('src','https://code.jquery.com/jquery.js');
	document.getElementsByTagName('body')[0].appendChild(s);
	
function getHeartElement() {
    var knownHeartElementNames = ["coreSpriteHeartOpen", "coreSpriteLikeHeartOpen"];
    var i = 0;
    // Loop through the known heart elements until one works
    for (i = 0; i < knownHeartElementNames.length; i++) {
        var heartElement = document.querySelector('.' + knownHeartElementNames[i]);
        if (heartElement != undefined) {
            break;
        }
    }
    return heartElement;
}

function doLike() {
	
	
    var likeElement = getHeartElement();
    var nextElement = document.querySelector('.coreSpriteRightPaginationArrow');
    likeCount++;
    console.log('Liked ' + likeCount);
    var nextTime = (Math.random() * 5000) + 1000;
	
	var FollowButton = document.querySelector('._qv64e');
	FollowButton.click();
	
	if ( getHeartElement() != null) {
		likeElement.click();
	}
    

    setTimeout(function() {nextElement.click();}, 1000);
    if (likeCount < 1000) {
        setTimeout(doLike, nextTime);
    } else {
        console.log('Nice! Time for a break.');
    }
}

var likeCount = 0;
doLike();
```
