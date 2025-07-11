<script>
	
	import '../app.css';

	let { children } = $props();
	import "../app.css"
</script>

<!-- <Navbar />  -->

{@render children()}
export const prerender = true;
