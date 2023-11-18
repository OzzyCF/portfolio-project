<script>
	import '../app.postcss';
	// Import the NavBar component
	import NavBar from '../lib/NavBar.svelte';
</script>

<header>
	<NavBar></NavBar>
</header>

<main>
	<!-- The <slot> element is where nested route content will be injected -->
	<slot />
</main>

<footer>
	<!-- You can also have footer content that will be present on every page -->
	<!-- Your footer content -->
</footer>

<style>
	/* Your global styles can also go here */
</style>
