	<html>
		<head>
			<title>{{ page.title }}</title>
			<!-- link to main stylesheet -->
			<link rel="stylesheet" type="text/css" href="/css/main.css">

			<script>
			  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
			  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new
			  Date();a=s.createElement(o),
			  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
			  })(window,document,'script','https://www.google-analytics.com/analytics.js','ga');

			  ga('create', 'UA-90240935-1', 'auto');
			  ga('send', 'pageview');

			  </script>
		</head>
		<body>
		  <table>
		    <tr>
		      <td>
			<img class="myimage" align="center" valign="top" src="https://www.cloudbees.com/sites/default/files/styles/headshot/public/harpreet_singh.png?itok=dhCpmDVi" alt="picture"/>
		      </td>
		      <td>
			<h1 class="myimage"> Harpreet Singh</h1>
		      </td>
		    </tr>
		  </table>

		  <nav>
	    	    <ul>
	        		<li><a href="/">Home</a></li>
		        	<li><a href="/about">About</a></li>
	        		<li><a href="https://www.linkedin.com/in/singhharpreet">LinkedIn</a></li>
	        		<li><a href="/blog">Blog</a></li>
	        		<li><a href="/now">Now</a></li>
				<li><a href="https://www.facebook.com/pg/harpreet.fireart/photos/?ref=page_internal">My Art</a></li>
	        		<li><a href="/books">Books</a></li>
	    		</ul>
		  </nav>

		  <div class="container">

			{{ content }}

			</div><!-- /.container -->
			<footer>
<!--	    		<ul>
	        		<li><a href="mailto:singh.harry@gmail.com">email</a></li>
<!--	        		<li><a href="https://github.com/harpreetsingh">github.com/harpreetsingh</a></li>
				</ul> -->
			</footer>
		</body>
	</html>
