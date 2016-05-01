	<html>
		<head>
			<title>{{ page.title }}</title>
			<!-- link to main stylesheet -->
			<link rel="stylesheet" type="text/css" href="/css/main.css">
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
