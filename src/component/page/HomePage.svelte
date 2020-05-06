<script>
	import { fly } from 'svelte/transition';
	import IconButton from '../button/IconButton.svelte';
	export let location;
	console.info("location:",location);
	let visible = true;
	const toggle=()=>{
		visible = !visible;
	}
</script>
<div transition:fly={{ x: -100, duration: 200 }} class="root">
	<div class="col-12 col-sm-10 col-md-7 col-lg-5 col-xl-3">
		This is the home page, and here's a button!
		{#if visible}
			<IconButton click={toggle} text="Hide me!" icon="close"/>
		{/if}
	</div>
</div>
<style lang="scss">
	.root{
		position: fixed;
		left: 0;
		right: 0;
		top: 0;
		bottom: 0;
		display: grid;
		grid-template-columns: auto;
		grid-auto-rows: 90vh;
		align-items: center;
		justify-items: center;
		overflow-y: auto;
	}
</style>