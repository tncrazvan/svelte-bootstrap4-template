<script>
	import SideMenu from './component/menu/SideMenu.svelte';
	import HomePage from './component/page/HomePage.svelte';
	import { Router, Route, navigate } from 'svelte-routing';

	//jquery
	//import './libs/jquery/jquery.min.js'; ====> imported directly in index.html

	//popper
	//import './libs/popper/popper.min.js'; ====> imported directly in index.html

	//bootstrap
	//import './libs/bootstrap/bootstrap.min.js' ====> imported directly in index.html;
	//import './libs/bootstrap/bootstrap.min.css'; ====> imported directly in index.html
	

	//datatables
	//import './libs/datatables/datatables.js'; ====> imported directly in index.html
	//import './libs/datatables/datatables.css'; ====> imported directly in index.html
	

	//datepicker
	import './libs/datepicker/datepicker.js';
	import './libs/datepicker/datepicker.css';

	//others
	import './style/fontawesome/css/all.min.css';
	import './style/extra.css';
	export let url = window.location.pathname;
	/*const getSidemenuData=async ()=>{
		let response = await fetch("/json/sidemenu.json");
		response = await response.json();
		return response;
	}
	let sidemenuData = getSidemenuData();*/
	let sidemenuData;
</script>
{#if sidemenuData}
	{#await sidemenuData}
		<span></span>
	{:then data}
		<SideMenu title={data.title} user={data.user} sections={data.sections}/>
	{:catch error}
		<span></span>
	{/await}
{/if}
<Router url="{url}">
	<Route path="/">
		<HomePage />
	</Route>
</Router>