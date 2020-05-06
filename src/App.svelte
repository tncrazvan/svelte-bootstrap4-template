<script>
import { Router, Route, navigate } from 'svelte-routing';
import HomePage from './component/page/HomePage.svelte';
import './materialicons/materialicons.css';
import './style/style.css';
export let url = window.location.pathname;
</script>

<Router url="{url}">
	<Route path="/home" component={HomePage} />
	<Route path="/" component={HomePage} />
</Router>