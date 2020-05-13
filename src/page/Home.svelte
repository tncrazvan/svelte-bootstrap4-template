<script>
	import SearchBar from './../shared/component/input/SearchBar.svelte';
	import { fly } from 'svelte/transition';
	let suggestions = [
		{value:"Print"},
		{value:"#asd"}
	];
	let tags = {
		"#asd": [
			{value:"asd"}
		]
	};
</script>
<div transition:fly={{ x: -100, duration: 200 }} class="page">
	<SearchBar suggestions={suggestions} tags={tags}/>
</div>