## 1. Open Your Instagram Account
## 2. Choose a Hashtag : example => Cats
## 3. Replace this with your hashtag : 
## https://www.instagram.com/explore/tags/{{hashtag}}
## Example : https://www.instagram.com/explore/tags/cats
## 4. Open The First Picture
## 5. Copy/Paste The code below in Console
## 6. Have Fun ♥

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
