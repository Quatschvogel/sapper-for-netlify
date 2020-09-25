<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script>import BlogBeitrag from "../components/blog_beitrag.svelte";

import Blogbeitrag from "../components/blog_beitrag.svelte";
let name = "Blogpost5";
let beschreibung = "Das hier ist die Beschreibung des neusten Blogposts";
</script>

<!--------------------------------------------------------------------------->
<!---------------------- CSS / BOOTSTRAP DER COMPONENTE --------------------->
<!--------------------------------------------------------------------------->
<style>

	.jumbotron {
		max-width: 750px;
		max-height: 750px;
		margin: auto;
		margin-top: 40px;
		margin-bottom: 30px;
		padding: 20px;
	}

	.containerBackground {
		margin-left: 5px;
		margin-right: 5px;
	}


</style>

<!--------------------------------------------------------------------------->
<!----------------------- HTML / MARKUP DER COMPONENTE ---------------------->
<!--------------------------------------------------------------------------->
<svelte:head>
	<title>Home</title>
</svelte:head>

<div class="jumbotron">
	<h1>Warum diese Website?</h1>
	<p style="font-size: 20px">Hier dann entsprechend die beschreibung warum diese Website entstanden ist und so weiter.....</p>
</div>

<div class="containerBackground">
<div class="jumbotron">
<div class="embed-responsive embed-responsive-16by9">
	<iframe 
		class="embed-responsive-item" 
		src="https://www.youtube.com/embed/DilHMEovGgY" 
		allowfullscreen
		title="Immore Video">
	</iframe>
</div>
</div>
<div style="height:20px;"></div>
</div>
<BlogBeitrag bind:name={name} bind:beschreibung={beschreibung}/>