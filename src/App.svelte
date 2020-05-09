<script>
	import Home from './page/Home.svelte';
	import Printing from './shared/page/Printing.svelte';
	import SideMenu from './shared/component/menu/SideMenu.svelte';
	import { Router, Route, navigate } from 'svelte-routing';
	import {printer} from './shared/store/printer.js';

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
	import './shared/libs/datepicker/datepicker.js';
	import './shared/libs/datepicker/datepicker.css';

	//others
	import './shared/style/fontawesome/css/all.min.css';
	import './shared/style/extra.css';
	import './shared/style/printable.css';

	
	export let url = window.location.pathname;
	const getSidemenuData=async ()=>{
		let response = await fetch("/json/sidemenu.json");
		response = await response.json();
		return response;
	}
	let sidemenuData = getSidemenuData();
</script>
{#if sidemenuData}
	{#await sidemenuData}
		<span></span>
	{:then data}
		{#if data.enabled}
			<SideMenu title={data.title} user={data.user} sections={data.sections}/>
		{/if}
	{:catch error}
		<span></span>
	{/await}
{/if}
{#if !$printer.showing}
<Router url="{url}">
	<Route path="/" component={Home}/>
	<Route path="/index.html" component={Home}/>
</Router>
{:else}
	<Printing />
{/if}