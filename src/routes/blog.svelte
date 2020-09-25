<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script>
	import BlogBeitrag from '../components/blog_beitrag.svelte'
	let name = "Kilian";

	let blogpost = [
		{
			name: "Blogpost 1",
			beschreibung: "Hier steht dann eine kurze beschreibung des Blogposts 1 wo ein grober Überblick gegeben werden kann."
		},
		{
			name: "Blogpost 2",
			beschreibung: "Hier steht dann eine kurze beschreibung des Blogposts 2 wo ein grober Überblick gegeben werden kann."
		},
		{
			name: "Blogpost 3",
			beschreibung: "Hier steht dann eine kurze beschreibung des Blogposts 3 wo ein grober Überblick gegeben werden kann."
		}
	]

</script>

<!--------------------------------------------------------------------------->
<!---------------------- CSS / BOOTSTRAP DER COMPONENTE --------------------->
<!--------------------------------------------------------------------------->
<style>

</style>

<!--------------------------------------------------------------------------->
<!----------------------- HTML / MARKUP DER COMPONENTE ---------------------->
<!--------------------------------------------------------------------------->
<svelte:head>
	<title>Blog</title>
</svelte:head>

{#each blogpost as blog}
	<BlogBeitrag bind:name={blog.name} bind:beschreibung={blog.beschreibung}/>
{/each}


