<script>
	import SideMenu from './component/menu/SideMenu.svelte';
	import HomePage from './component/page/HomePage.svelte';
	import { Router, Route, navigate } from 'svelte-routing';
	import './style/fontawesome/css/all.min.css';
	import './style/style.css';
	export let url = window.location.pathname;
	const getSidemenuData=async ()=>{
		let response = await fetch("/json/sidemenu.json");
		response = await response.json();
		return response;
	}
	let sidemenuData = getSidemenuData();
</script>
{#await sidemenuData}
	<span></span>
{:then data}
	<SideMenu title={data.title} user={data.user} sections={data.sections}/>
{:catch error}
	<span></span>
{/await}
<Router url="{url}">
	<Route path="/">
		<HomePage />
	</Route>
</Router>