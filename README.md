### Back-to-top-using-Jquery

Implementing simple back to top button using Jquery.

On clicking, the button/image takes the user to the top of the page; Saves the user time as well as improves the user experience.

Both image and a clickable link can used for the functionality

```javascript
The main Jquery code for implementing back to top functionality-

<script type="text/javascript">
// create the back to top button
$('body').prepend('<a href="#" class="back-to-top">Back to Top</a>');  //clickable icon for Back to Top

var amountScrolled = 300;

$(window).scroll(function() {
	if ( $(window).scrollTop() > amountScrolled ) {
		$('a.back-to-top').fadeIn('slow');
	} else {
		$('a.back-to-top').fadeOut('slow');
	}
});

$('a.back-to-top, a.simple-back-to-top').click(function() {
	$('html, body').animate({
		scrollTop: 0
	}, 700);
	return false;
});
</script>
```

**up-arrow.png** is the png file for the back-to-top image

**simple-back-to-top** is the class for the Back to Top clickable button/link

**styles.css** is the css files that contains **back-to-top** class which calls up-arrow.png image 
file
