<script>
	import DatePicker from './../input/DatePicker.svelte';
	import SplitLoginForm from './../form/SplitLoginForm.svelte';
	import FloatingRegistrationForm from './../form/FloatingRegistrationForm.svelte';
	import FloatingLoginForm from './../form/FloatingLoginForm.svelte';
	import { fly } from 'svelte/transition';
</script>
<div transition:fly={{ x: -100, duration: 200 }} class="root">
	<SplitLoginForm submit={data=>console.log(data)} image={"/assets/images/fox.png"}/>
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