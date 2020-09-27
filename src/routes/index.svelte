<!--------------------------------------------------------------------------->
<!------------------------ JAVASCRIPT DER COMPONENTE ------------------------>
<!--------------------------------------------------------------------------->
<script context="module">
	export function preload() {
		return this.fetch(`blog.json`).then(r => r.json()).then(posts => {
			return { posts };
		});
	}
</script>
<script>
	import BlogBeitrag from "../components/blog_beitrag.svelte";
	import Postlist from "../components/postlist.svelte";
	import YoutubeVideo from '../components/youtube_video.svelte'
	import { onMount } from 'svelte';

  onMount(() => {
    if (window.netlifyIdentity) {
      window.netlifyIdentity.on("init", user => {
        if (!user) {
          window.netlifyIdentity.on("login", () => {
            document.location.href = "/admin/";
          });
        }
      });
    }
  });
  export let posts;
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
	<script src="https://identity.netlify.com/v1/netlify-identity-widget.js"></script>
</svelte:head>

<div class="jumbotron">
	<h1>Warum diese Website?</h1>
	<p style="font-size: 20px">Hier dann entsprechend die beschreibung warum diese Website entstanden ist und so weiter.....</p>
</div>

<YoutubeVideo/>
<BlogBeitrag bind:name={posts[0].title} bind:beschreibung={posts[0].title}/>
<Postlist/> 