<script>
	import Nav from '../components/Nav.svelte';
	export let segment;
	export let tog;
</script>

<style>
	main {
		position: relative;
		background-color: white;
		margin: 0 auto;
		box-sizing: border-box;
	}
	.noScrolling {
		position: relative;
		max-width: 56em;
		background-color: white;
		padding: 2em;
		margin: 0 auto;
		box-sizing: border-box;
		touch-action: none;
	}
</style>

<Nav {segment} {tog}/>

<main class="{tog == true ? "noScrolling" : ""}">
	<slot></slot>
</main>