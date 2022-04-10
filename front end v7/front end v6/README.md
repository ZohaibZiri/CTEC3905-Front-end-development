******************
**	Aram Saeed	**
**	Unit 10		**
**	10/05/2021	**
******************

# Validate by File Upload
https://validator.w3.org/#validate_by_upload

# Adding images and json file for the social media

# HTML lang="en"

	<title>
	<link>
	<meta>


	<header>
	</header>

	<nav>
		<a href="url">link text</a>
		...
		<a href="#">Contact Us</a>
		<a href="https://www.w3schools.com/">Visit W3Schools.com!</a>
		
		All buttons have been deleted ...
		<button type="button">Click Me!</button>
		<button class="button"><a href="#">Products</a></button>
		<button class="button"><a href="https://www.w3schools.com/">W3Schools</a></button>
		<button class="button"><a href="https://www.tutorialspoint.com/html/index.htm"><span>Tutorials Point</span></a></button>
		<button class="button" style="float:right"><a href="https://www.tutorialspoint.com/html/index.htm"><span>Tutorials Point</span></a></button>
		...
		
		# style add to the last 2 buttons
			- style="float:right"
		<ul>
			<li class="button"><a href="#product"><span>Products</span></a></li>
			<li class="button"><a href="#service"><span>Services</span></a></li>
			<li class="button"><a href="#legal"><span>Legal Terms</span></a></li>
			<li class="button"><a href="#contact"><span>Contact Us</span></a></li>
			<li class="button" style="float:right" ><a href="https://www.w3schools.com/"><span>W3Schools</span></a></li>
			<li class="button" style="float:right" ><a href="https://www.tutorialspoint.com/html/index.htm"><span>Tutorials Point</span></a></li>
		</ul>
		
		# new structure
		<ul id="navbar">
			<li class="button" onclick="myFunction()" style="float:right"><span>Search</span></a></li>
			<li><input type="search" id="mySearch" placeholder="Search for something..."></li>
			<li class="button"><a href="#product"><span>Products</span></a></li>
			<li class="button"><a href="#service"><span>Services</span></a></li>
			<li class="button"><a href="#legal"><span>Legal Terms</span></a></li>
			<li class="button"><a href="#contact"><span>Contact Us</span></a></li>
		</ul>
	</nav>

	<section>
	</section>

	<article>
		<h1>Article</h1>
		<div id="product">
			<h2>Product</h2>
		</div>
		<div id="service">
			<h2>Service</h2>
		</div>
	</article>

	<aside>
		<h1>Aside</h1>
		<div id="legal">
			<h2>Legal</h2>
		</div>
		<div id="contact">
			<h2>Contact</h2>
		</div>
	</aside>

	<footer>
		<a href="https://twitter.com/"><img alt="twitter" src="twitter.png" width="70" height="70">	deleted
		<div id="soc_med"></div> added
	</footer>


# STYLESHEET

	_style	
		*
		{
			box-sizing: border-box;
			margin-left: 3%;	removed
			margin-right: 3%;	removed
		}
		
		body
			color: #000000;
			margin-left: 5%;
			margin-right: 5%;
			
		header
			background-color: #d6f5d6;
			margin-top: 80px;
		
		nav  - deleted
			background-color: #cce6ff; - deleted
			padding: 10px; - deleted
			text-align: left; - deleted
			font-size: 20px; - deleted
			height: 70px; - deleted
			margin-bottom: 10px; - deleted
			border-radius: 5px 25px 10px; - deleted
		ul
		{
			list-style-type: none;
			margin: 1%;
			padding: 0;
			overflow: hidden;
		}
		.navbar
		{
			overflow: hidden;
			position: fixed;
			top: 0;
			width: 100%;	changed
			width: 85%;
		}
		
		#navbar input[type=search]
		{
			float: right;
			padding: 10px;
			margin-right: 5px;
			font-size: 20px;
			border: 2px solid #008CBA;
			border-radius: 10px;
		}
		
		section
		
		article
			color: white; or color: #ffffff;
			height: 200px; - deleted
		#product, service
		{
			height:500px;
			background-color: #;
		}		
		
		
		aside
			height: 200px; - deleted
		#legal, contact
		{
			height:500px;
			background-color: #;
		}
		
		footer
			background-color: #f2d9e6;
			height: 125px;
			
		#soc_med
		{
			float: right;
			padding: 1%;
		}

		
		/* Responsive layout - on tablet screens */
		@media (max-width: 600px)
		{
			*
			{
				box-sizing: border-box;
				margin-left: 1%;
				margin-right: 1%;
			}
			
			header, nav, section, article, aside, footer
			{
				width: 100%;
				height: auto;
			}
		}

		/* Responsive layout - on mobile screens */
		@media (max-width: 420px)
		{
			*
			{
				box-sizing: border-box;
				margin-left: 0%;
				margin-right: 0%;
			}
			
			header, nav, section, article, aside, footer
			{
				width: 100%;
				height: auto;
			}
		}
		
	_button
		.button
			width: 150px;
		.button:hover
			box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24),0 17px 50px 0 rgba(0,0,0,0.19);
		.button span
		.button span:after
		.button:hover span
		.button:hover span:after

# JAVASCRIPT

	_script
		function Para_Func(){
			document.getElementById("target").innerHTML = "The Internet of Things (IoT) is the term which refers to the ever-growing network of physical objects with embedded sensors which can connect together via the internet allowing communication to occur between these objects and many other Internet-enabled devices and systems.";
		}
		function myFunction(arr){
			let out = "";
			let i;
			for(i = 0; i < arr.length; i++)	{	
				out += '<a href="' + arr[i].url + '">' + '<img src=" ' + arr[i].img + '" width="75" height="75">' + '</a>';
			}
			document.getElementById("soc_med").innerHTML = out;
		}
		function mySearch(){
			var x = document.getElementById("my_search").placeholder;
			document.getElementById("demo").innerHTML = x;
		}
		
	_soc_med
		myFunction([
			{"display": "facebook", "url": "https://www.facebook.com", "img" : "icon_1.png" },
			{"display": "twitter", "url": "https://twitter.com", "img" : "icon_2.png" },
			{"display": "Linkedin", "url": "https://www.linkedin.com", "img" : "icon_3.png" },
			{"display": "Youtube", "url": "https://www.youtube.com", "img" : "icon_4.png" },
			{"display": "Pinterest", "url": "https://www.pinterest.co.uk", "img" : "icon_5.png" }
		])