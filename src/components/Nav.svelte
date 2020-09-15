<script>
	export let segment;
</script>

<style>
	img {
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
	}

</style>
<section>
	<div class="row text-center">
		<div class="jumbotron containerFix" style="padding:0;margin:0" >
			<img src="successkid.jpg" alt="Success Kid" class="img-fluid" style="border-radius: 50px">
		</div>
	</div>
</section>
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
			<a 	aria-current="{segment === undefined ? 'page' : undefined}" 
				href="." 
				class="{segment === undefined ? "active" : ""}">
				Home
			</a>
		  </li>
		  <li class="nav-item">
			<a 	aria-current="{segment === 'about' ? 'page' : undefined}" 
				href="about"
				class="{segment === 'about' ? "active" : ""}">
				About
			</a>
		  </li>
		  <li class="nav-item">
			<a 	rel=prefetch 
				aria-current="{segment === 'blog' ? 'page' : undefined}" 
				href="blog"
				class="{segment === 'blog' ? "active" : ""}">
				Blog
			</a>
		  </li>
		</ul>
	  </div>
</nav>