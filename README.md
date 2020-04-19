# JQLoader
JQLoader is a Jquery plugin to show a loading bar, or full screen loading

# Usage

Just include `JQLoader.css` and `JQLoader.js` in your HTML page.

Full code sample :

```html
<!-- Only for beautify this demo page -->
<style>
body{
font-family:calibri;
}

.div_sample{
width:200px;
height:200px;
border:1px solid #dedede;
}
</style>

<!-- Loading need this -->
<script src="jquery.js" type="text/javascript"></script>
<script src="jquery.easing.min.js" type="text/javascript"></script>

<!-- Loading Core -->
<link rel="stylesheet" type="text/css" href="css/JQLoader.css" />
<script src="js/JQLoader.js" type="text/javascript"></script>

<h1>JQLoader</h1>
<h3>JQLoader is a Jquery plugin to show a loading bar, or full screen loading</h3>

Try our the Sample : <br/><br/>

<h2>Full Screen Loading</h2>

<h3>Standard Theme</h3>
<button id="open_standard">Open Standard</button>
<button id="close_standard">Close Standard</button>

<h3>Bottom Bar Theme</h3>
<button id="open_bottom">Open</button>
<button id="close_bottom">Close</button>

<h2>Loading on the div</h2>

<button id="open_div_standard">Open div Standard</button>
<button id="close_div_standard">Close div Standard</button>
<br/><br/>
<div style="position:relative;" class="div_sample"></div>

<script>

$(document).ready(function(){

	// Full screen standard
	$('#open_standard').click(function(){
		
		$( "body" ).JQLoader({
			theme: "standard",
			mask: true,
			background: "#444",
			color: "#fff"
		});
		
	});
	
	$('#close_standard').click(function(){
	
		$( "body" ).JQLoader({
			action: "close"
		});
		
	});
	
	// Div standard
	$('#open_div_standard').click(function(){
	
		$( ".div_sample" ).JQLoader({
			theme: "standard",
			mask: true,
			background: "#fff",
			color: "#fff"
		});
		
	});
	
	$('#close_div_standard').click(function(){
	
		$( ".div_sample" ).JQLoader({
			theme: "standard",
			mask: true,
			background: "#fff",
			color: "#fff",
			action: "close"
		});
		
	});
	
	// Full screen
	$('#open_bottom').click(function(){
	
		$( "body" ).JQLoader({
			theme: "bottom",
			action: "open"
		});
		
	});
	
	$('#close_bottom').click(function(){
	
		$( "body" ).JQLoader({
			theme: "bottom",
			action: "close"
		});
		
	});
})
</script>
```
