<script>
	import Nav from '../components/Nav.svelte';
	import Footer from '../components/footer.svelte';
	export let segment;
	export let tog;
</script>

<style>

.foot-flex {
	display: flex;
	flex-direction: column;
	min-height: 100vh;
}

.flex-grow {
	flex-grow: 1;
}


</style>
<div class="foot-flex">
<Nav {segment} {tog}/>


	<slot></slot>
<div class="flex-grow"></div>



<Footer/>
</div>