<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script>

</script>

<!--------------------------------------------------------------------------->
<!---------------------- CSS / BOOTSTRAP DER COMPONENTE --------------------->
<!--------------------------------------------------------------------------->
<style>
	.container-fluid {
		margin-top: 20px;
	}
	.containerHintergrund {
		background: #e9ecef;
		width: 97%;
		height: 200px;
		border: 1px solid transparent;
		border-radius: 10px;
		margin-bottom: 20px;

	}

	.containerHintergrund h1 {
		padding-top: 10px;
		padding-left: 10px;
		color: black;
	}
	.containerHintergrund h4 {
		padding-top: 35px;
		padding-left: 10px;
		padding-right: 10px;
		color: black;
		font-weight: normal;
		font-size: 18px;
	}

	.middle {
		justify-content: center;
		display: flex;
		padding: 0;
		margin: 0;
	}

	.btn-success {
		display: flex;
		margin-left: 70%;
	}

	@media screen and (max-width: 768px) {
		.no-Padding {
			padding: 0 !important;
			width: 100%;
			margin: 0 !important;
		}
		.btn-success {
			display: flex;
			margin-left: 80%;
			margin-top: 5%;
		}
	}

	@media screen and (max-width: 350px) {
		.btn-success {
			display: flex;
			margin-left: 30%;
			margin-top: 0%;
		}
	}
	
	@media screen and (max-width: 450px) {
		.btn-success {
			display: flex;
			margin-left: 65%;
			margin-top: 0%;
		}
	}

	@media screen and (min-width: 768px) {
		.containerHintergrund {
			background: #e9ecef;
			width: 450px;
			height: 200px;
			border: 1px solid transparent;
			border-radius: 10px;
		}
		.no-Padding {
			padding: 0 !important;
			width: 1000px;
		}
	}

</style>

<!--------------------------------------------------------------------------->
<!----------------------- HTML / MARKUP DER COMPONENTE ---------------------->
<!--------------------------------------------------------------------------->
<svelte:head>
	<title>Blog</title>
</svelte:head>
<div class="container-fluid no-Padding">
<div class="row">
	<div class="col-md-12 col-lg-6 col-xl-6 middle">
		<div class="containerHintergrund">
			<h1>Blogpost1</h1>
			<h4>Hier steht dann immer einer kleine kurz beschreibung des Blogposts</h4>
			<button class="btn btn-success">Mehr lesen</button>
		</div>
	</div>
	<div class="col-md-12 col-lg-6 col-xl-6 middle">
		<div class="containerHintergrund">
			<h1>Blogpost2</h1>
			<h4>Hier steht dann immer einer kleine kurzbeschreibung des Blogposts</h4>
			<button class="btn btn-success">Mehr lesen</button>
		</div>
	</div>
	<div class="col-md-12 col-lg-6 col-xl-6 middle">
		<div class="containerHintergrund">
			<h1>Blogpost3</h1>
			<h4>Hier steht dann immer einer kleine kurzbeschreibung des Blogposts</h4>
			<button class="btn btn-success">Mehr lesen</button>
		</div>
	</div>
	<div class="col-md-12 col-lg-6 col-xl-6 middle">
		<div class="containerHintergrund">
			<h1>Blogpost3</h1>
			<h4>Hier steht dann immer einer kleine kurzbeschreibung des Blogposts</h4>
			<button class="btn btn-success">Mehr lesen</button>
		</div>
	</div>
</div>
</div>