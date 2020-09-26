<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script>
	import BlogBeitrag from '../components/blog_beitrag.svelte'
	import { onMount } from 'svelte';

	let blogpost = [];

	onMount(async () => {
		const res = await fetch('http://localhost:8888/wordpress/wp-json/wp/v2/posts');
		const json = await res.json();
		blogpost = json 
	});
	

	

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

<div style="height:30px"></div>
{#each blogpost as blog}
	<BlogBeitrag bind:name={blog.title.rendered} bind:beschreibung={blog.beschreibung}/>
{/each}


