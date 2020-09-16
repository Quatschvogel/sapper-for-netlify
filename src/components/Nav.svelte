<script>
	export let segment;
	let tog = false;

		function onClick () {
			tog = !tog;
		}
	
</script>

<style>
	/* img {
		height: 100%;
		width: 70%;
		padding-top: 10px;
		padding-bottom: 10px;
	}
	
	.containerFix {
		height: 200px;
	}

	.active {
		color:firebrick;
	}

	a:hover {
		color: firebrick;
		text-decoration: none;
	}

	a {
		color: white;
		font-size: 20px;
		padding-right: 20px;
	}*/

	nav {
		height: 10vh;
		background: #5b78c7;
		position: sticky;
		top: 0;
		z-index: 20;
	}

	.nav-links {
		display: flex;
		list-style: none;
		width: 50%;
		height: 100%;
		justify-content: space-around;
		align-items: center;
		margin-left: auto;
	}

	.nav-links li a {
		color: white;
		text-decoration: none;
		font-size: 16px;
	}

	.active {
		color: darkred;
	}

	.nav-links li a:hover {
		color: darkred;
	}

	@media screen and (max-width: 768px) {
		.nav-links {
			flex-direction: column;
			position: fixed;
			background: #5b78c7;
			height: 100vh;
			width: 100%;
			clip-path: circle(20px at 100% -10%);
			-webkit-clip-path: circle(20px at 100% -10%);
			transition: all 1s ease-out;
		}

		.nav-links.open {
			clip-path: circle(1000px at 100% -10%);
			-webkit-clip-path: circle(1000px at 100% -10%);
		}

		.line {
			width: 30px;
			height: 3px;
			background: white;
			margin: 5px;
		}

		nav {
			position: sticky;
			top:0;
			width: 100%;
			z-index: 20;
		}

		.hamburger {
			position: absolute;
			cursor: pointer;
			right: 5%;
			top: 50%;
			z-index: 50;
			transform: translate(-5%, -50%);
			
		}
	}

.containerFix {
	height: 50px;
	width: 100%;
	justify-content: center;
	text-align: center;
}

</style>
<!--
<section>
	<div class="row text-center">
		<div class="jumbotron containerFix" style="padding:0;margin:0" >
			<img src="successkid.jpg" alt="Success Kid" class="img-fluid" style="border-radius: 50px">
		</div>
	</div>
</section>
-->
<div class="containerFix"><h1>Hier ist dann das Logo</h1></div>
<nav>
	<div class="hamburger" on:click={onClick}>
		<div class="line"></div>
		<div class="line"></div>
		<div class="line"></div>
	</div>
	<ul class="{tog == false ? 'nav-links' : 'nav-links open'}">
		<li><a 	aria-current="{segment === undefined ? 'page' : undefined}" 
			href="." 
			class="{segment === undefined ? "active" : ""}" on:click={onClick}>
			Home
		</a></li>
		<li><a 	aria-current="{segment === 'about' ? 'page' : undefined}" 
			href="about"
			class="{segment === 'about' ? "active" : ""}" on:click={onClick}>
			About
		</a></li>
		<li><a 	rel=prefetch 
			aria-current="{segment === 'blog' ? 'page' : undefined}" 
			href="blog"
			class="{segment === 'blog' ? "active" : ""}" on:click={onClick}>
			Blog
		</a></li>
	</ul>
</nav>









<!--
<nav class="navbar navbar-expand-sm navbar-dark bg-dark sticky-top">
	<div class="navbar-brand" style="padding-right:30px; font-size:25px;">Immore</div>
	<button 
		class="navbar-toggler" 
		type="button" 
		data-toggle="collapse" 
		data-target="#navbarNav" 
		aria-controls="navbarNav" 
		aria-expanded="false" 
		aria-label="Toggle navigation">
		<span class="navbar-toggler-icon"></span>
	</button>
	<div class="collapse navbar-collapse" id="navbarNav">
		<ul class="navbar-nav">
		  <li>
			
		  </li>
		  <li class="nav-item">
			
		  </li>
		  <li class="nav-item">
			
		  </li>
		</ul>
	  </div>
</nav>
-->