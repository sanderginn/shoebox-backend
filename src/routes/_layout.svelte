<script>
	import 'bootstrap/dist/css/bootstrap.min.css';
	import '@fortawesome/fontawesome-free/css/all.css';

	import Nav from '../components/Nav.svelte';
	import Container from 'sveltestrap/src/Container.svelte';
	export let segment;
</script>

<style>
	main {
		position: relative;
		max-width: 56em;
		background-color: white;
		padding: 2em;
		margin: 0 auto;
		box-sizing: border-box;
	}
</style>

<Nav {segment}/>

<Container>
<main>
	<slot></slot>
</main>
</Container>