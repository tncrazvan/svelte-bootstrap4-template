<script>
	import { Router, Route, navigate } from 'svelte-routing';
	import Home from './page/Home.svelte';
	export let url; //this is your application window.location.pathname
</script>
<Router url="{url}">
	<Route path="/" component={Home}/>
	<Route path="/index.html" component={Home}/>
</Router>