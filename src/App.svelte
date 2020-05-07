<script>
	import HomePage from './component/page/HomePage.svelte';
	import { Router, Route, navigate } from 'svelte-routing';
	import './style/fontawesome/css/all.min.css';
	import './style/style.css';
	export let url = window.location.pathname;
	
	
</script>

<Router url="{url}">
	<Route path="/">
		<HomePage />
	</Route>
</Router>