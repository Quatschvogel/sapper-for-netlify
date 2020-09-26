<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script>
	import BlogBeitrag from "../components/blog_beitrag.svelte";
	import Postlist from "../components/postlist.svelte";
	import YoutubeVideo from '../components/youtube_video.svelte'

	let name = "Blogpost5";
	let beschreibung = "Das hier ist die Beschreibung des neusten Blogposts";
</script>

<!--------------------------------------------------------------------------->
<!---------------------- CSS / BOOTSTRAP DER COMPONENTE --------------------->
<!--------------------------------------------------------------------------->
<style>

	.jumbotron {
		width: 90%;
        max-width: 50rem;
		max-height: 750px;
		margin: auto;
		margin-top: 40px;
		margin-bottom: 30px;
		padding: 20px;
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

<YoutubeVideo/>
<BlogBeitrag bind:name={name} bind:beschreibung={beschreibung}/>
<Postlist/> 