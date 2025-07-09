<script>
	import Navbar from '$lib/Navbar.svelte';
import '../app.css';

	let { children } = $props();
	import "../app.css"
</script>

<Navbar /> 

{@render children()}
