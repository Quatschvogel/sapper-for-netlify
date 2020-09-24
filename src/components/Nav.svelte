
<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script>
	export let segment;
	export let tog = false;

	function onClick () {
			tog = !tog;
	}
	
</script>

<!--------------------------------------------------------------------------->
<!---------------------- CSS / BOOTSTRAP DER COMPONENTE --------------------->
<!--------------------------------------------------------------------------->
<style>
	nav {
		height: 50px;
		background: #008ACD;
		position: sticky;
		top: 0;
		z-index: 20;
		display: block;
	}

	.nav-links {
		display: flex;
		list-style: none;
		width: 30%;
		height: 100%;
		justify-content: space-between;
		align-items: center;

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
	
	.containerFix {
		height: 50px;
		width: 100%;
		justify-content: center;
		text-align: center;
	}

	.containerFix h1 {
		height: 100%;
		padding-top: 5px;
		padding-bottom: 5px;
		font-size: 30px;
	}


	@media screen and (max-width: 768px) {
		.nav-links {
			flex-direction: column;
			position: relative;
			background: #008ACD;
			height: 50vh;
			width: 100%;
			margin-left: auto;
			margin-right: auto;
			padding-top: 30%;
			clip-path: circle(20px at 0% -10%);
			-webkit-clip-path: circle(20px at 0% -10%);
			transition: all 0.4s ease-out;
			justify-content: space-between;
		}
		.nav-links.open {
			margin: auto;
			width: 100%;
			padding-right: 25%;
			padding-left: 25%;
			padding-bottom: 20%;
			height: 60hv;
			justify-content: space-between;
			clip-path: circle(1000px at 0% -10%);
			-webkit-clip-path: circle(1000px at 0% -10%);
		}

		.nav-links li a {
			font-size: 30px;
		}

		.line {
			width: 30px;
			height: 3px;
			background: white;
			margin: 5px;
		}
		.lineMiddle {
			width: 22px;
			height: 3px;
			background: white;
			margin: 5px;
		}

		.lineEnd {
			width: 14px;
			height: 3px;
			background: white;
			margin: 5px;
		}

		nav {
			position: sticky;
			top:0;
			width: 100%;
			z-index: 20;
			display: block;
		}

		.hamburger {
			position: absolute;
			cursor: pointer;
			left: 5%;
			top: 50%;
			z-index: 50;
			transform: translate(-5%, -50%);
		}

	}

</style>

<!--------------------------------------------------------------------------->
<!----------------------- HTML / MARKUP DER COMPONENTE ---------------------->
<!--------------------------------------------------------------------------->
<div class="containerFix"><h1>Hier ist dann das Logo</h1></div>
<nav>
	<div class="hamburger" on:click={onClick}>
		<div class="line"></div>
		<div class="lineMiddle"></div>
		<div class="lineEnd"></div>
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
			Blog
		</a></li>
		<li><a 	rel=prefetch 
			aria-current="{segment === 'blog' ? 'page' : undefined}" 
			href="blog"
			class="{segment === 'blog' ? "active" : ""}" on:click={onClick}>
			Über uns
		</a></li>
	</ul>
</nav>