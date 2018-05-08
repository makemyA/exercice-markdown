<!DOCTYPE html>
<html lang='en'>
<head>
	<meta charset='utf-8'>
	<meta http-equiv='X-UA-Compatible' content='IE=edge,chrome=1'>
	<meta name='viewport' content='width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no'>
	<title>un guide pour bien commencer avec markdown - Waxo</title>
	<meta name='author' content='Fabien Huet'>
	<meta name='description' content='Waxo'>
	<link rel=icon href=/assets/images/favicon.ico>
	<link href='/assets/styles/main.css' rel='stylesheet' type='text/css'>
	<link rel=author href='https://plus.google.com/u/0/108215978680291843501'>
	<link rel=publisher href='https://plus.google.com/u/0/108215978680291843501'>
	<meta name=keywords content='web developper, meteor, react, node'>
	<meta property=og:type content=site>
	<meta property=og:url content=http://wax-o.com/img>
	<meta property=og:title content='Fabien Huet, web developper'>
	<meta property=og:site_name content=waxo>
	<meta property=og:locale content=en_US>
	<meta property=og:description content='Hello, I’m Fabien, web ninja and food lover.'>
	<meta property=og:image content=http://wax-o.com/img/fabien_huet.png>
	<meta itemprop=name content='Fabien Huet, web developper'>
	<meta itemprop=description content='Hello, I’m Fabien, web ninja and food lover.'>
	<meta itemprop=image content=http://wax-o.com/img/fabien_huet.png>
	<meta name=twitter:card content=summary>
	<meta name=twitter:site content=@fabien_huet>
	<meta name=twitter:title content='Fabien Huet'>
	<meta name=twitter:description content='Hello, I’m Fabien, web ninja and food lover.'>
	<meta name=twitter:creator content=@fabien_huet>
	<meta name=twitter:image content=http://wax-o.com/img/fabien_huet.png>
</head>
<body>
<nav id='sideBar'>
	<div>
		<img src='/assets/images/fabien_huet.png' alt='Fabien Huet'>
		<h1>Fabien Huet</h1>
		<p>French web ninja <br> and food lover.</p>
	</div>
	<menu>
		<a href='/'>
			Home
			<svg xmlns='http://www.w3.org/2000/svg'>
				<path d='M10 20v-6h4v6h5v-8h3L12 3 2 12h3v8z'/>
			</svg>
		</a>
		<a target='_blank' href='https://github.com/fabien-h'>
			Github
			<svg xmlns='http://www.w3.org/2000/svg'>
				<path d='M22,12c0-5.5-4.5-10-10-10S2,6.5,2,12c0,4.6,3.1,8.4,7.2,9.6c0.1-0.1,0.2-0.2,0.2-0.3c0.2-0.5,0-1.3,0-1.9 c-1,0.2-2.3,0.2-3.1-0.6C6,18.5,6,18.1,5.8,17.7c-0.3-0.5-0.6-0.8-1-1.1C4.4,16.3,4.3,16,4.9,16c0.5,0,1.1,0.4,1.4,0.8 c0.4,0.5,0.6,1,1.2,1.3c0.6,0.2,1.4,0.1,2-0.1c0.1-0.6,0.3-1.1,0.7-1.4c-1.8-0.2-3.6-0.9-4.3-2.7C5.2,12.1,5.2,10,6.5,8.7 C6.1,7.9,6.2,6.9,6.6,5.9C7.4,5.7,8.7,6.5,9.4,7c1.7-0.5,3.5-0.5,5.2,0c0.7-0.5,1.9-1.4,2.8-1.1c0.4,1,0.4,1.9,0.1,2.7 c1.3,1.4,1.3,3.5,0.7,5.1c-0.7,1.8-2.5,2.5-4.3,2.7c1,0.9,0.7,2.8,0.7,4c0,0.4-0.1,0.9,0.2,1.1C18.9,20.4,22,16.6,22,12z'/>
			</svg>
		</a>
		<a target='_blank' href='http://wax-o.com/'>
			About me
			<svg xmlns='http://www.w3.org/2000/svg'>
				<path d='M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z'/>
			</svg>
		</a>
	</menu>
	<!-- 	<a href='/categories'><svg xmlns='http://www.w3.org/2000/svg'><path d='M19.5,9L9,19.5c-0.6,0.6-1.6,0.6-2.3,0l-6.3-6.3c-0.6-0.6-0.6-1.6,0-2.3L11,0.5C11.4,0.1,11.8,0,12.3,0l0,0 l5.5,1.2l0,0c0.2,0,0.8,0.2,1,1l1.1,5C20.1,7.9,20,8.5,19.5,9z M16.9,3.1c-0.6-0.6-1.7-0.6-2.3,0c-0.6,0.6-0.6,1.7,0,2.4 c0.6,0.6,1.7,0.6,2.4,0C17.5,4.8,17.5,3.8,16.9,3.1z'/></svg>Categories</a>
		<a href='/archives'><svg xmlns='http://www.w3.org/2000/svg'><path d='M19.3,0.1H0.7C0.3,0.1,0,0.3,0,0.7v3.1c0,0.4,0.3,0.7,0.7,0.7h18.7c0.4,0,0.7-0.3,0.7-0.7V0.7 C20,0.3,19.7,0.1,19.3,0.1z'/><path d='M0.4,5v7.9v1.2v4.7c0,0.6,0.5,1.2,1.2,1.2h16.8c0.6,0,1.2-0.5,1.2-1.2V14v-1.2V5H0.4z M14.2,9.1 c0,0.3-0.2,0.5-0.5,0.5H6.1c-0.3,0-0.5-0.2-0.5-0.5v-1c0-0.3,0.2-0.5,0.5-0.5h7.6c0.3,0,0.5,0.2,0.5,0.5V9.1z'/></svg>Archives</a> -->
</nav>
<article itemscope itemType='http://schema.org/BlogPosting' id='postContainer'>

	<header>
		<h1 itemprop='headline'>un guide pour bien commencer avec markdown</h1>
		<p>
			<time itemprop='datePublished' content='Tue Apr 08 2014 00:00:00 GMT+0200'>Apr 08, 2014</time>
			 in <a class="category-link" href="/categories/Code-fr/">Code fr</a> 
		</p>
