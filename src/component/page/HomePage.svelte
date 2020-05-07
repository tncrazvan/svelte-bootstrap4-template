<script>
	import Portfolio from './../misc/Portfolio.svelte';
	import { fly } from 'svelte/transition';
	let pages = [];
	pages.push([
			{title: "title 1",imageSrc: "/assets/images/java.png",description: "subtitle 1"},
			{title: "title 1",imageSrc: "/assets/images/java.png",description: "subtitle 1"},
			{title: "title 1",imageSrc: "/assets/images/java.png",description: "subtitle 1"}
	]);
	pages.push([
			{title: "title 2",imageSrc: "/assets/images/java.png",description: "subtitle 1"},
			{title: "title 2",imageSrc: "/assets/images/java.png",description: "subtitle 1"},
			{title: "title 2",imageSrc: "/assets/images/java.png",description: "subtitle 1"}
	]);
	pages.push([
			{title: "title 3",imageSrc: "/assets/images/java.png",description: "subtitle 1"},
			{title: "title 3",imageSrc: "/assets/images/java.png",description: "subtitle 1"},
			{title: "title 3",imageSrc: "/assets/images/java.png",description: "subtitle 1"}
	]);
</script>
<div transition:fly={{ x: -100, duration: 200 }} class="root">
	<Portfolio title="My projects" subtitle="Some of my projects" pages={pages} index={0}/>
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
		align-items: center;
		justify-items: center;
		overflow-y: auto;
	}
</style>