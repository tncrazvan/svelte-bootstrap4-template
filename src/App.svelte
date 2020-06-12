<script>
	import HomePage from './component/page/HomePage.svelte';
	import { Router, Route } from "svelte-routing";

	import '../node_modules/materialize-css/dist/js/materialize.min.js';
	import './style/fonts/Roboto/Roboto.css';
	import './style/materialicons/materialicons.css';
	import './style/materialize/materialize.css';
	import './style/scrollbar/scrollbar.css';
	import './style/margin/margin.css';
	import './style/padding/padding.css';
	import './style/waves/waves.css';
	import './style/_main/_main.css';

	let url = window.location.pathname;
</script>
<Router url="{url}">
    <Route path="/" component="{HomePage}" />
    <Route path="/index.html" component="{HomePage}" />
</Router>