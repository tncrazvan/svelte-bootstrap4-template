<script>
	import FloatingRegistrationForm from './../shared/component/form/FloatingRegistrationForm.svelte';
	import { fly } from 'svelte/transition';
</script>
<div transition:fly={{ x: -100, duration: 200 }} class="page">

	<FloatingRegistrationForm image={"/assets/images/logo.png"} />

</div>