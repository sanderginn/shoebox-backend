<script>
	import Navbar from 'sveltestrap/src/Navbar.svelte';
	import NavbarBrand from 'sveltestrap/src/NavbarBrand.svelte';
	import NavLink from 'sveltestrap/src/NavLink.svelte';
	export let segment;
</script>

<Navbar>
	<NavbarBrand href="/">Shoebox</NavbarBrand>
	<NavLink class={segment === undefined ? 'active' : undefined} href=".">home</NavLink>
	<NavLink class={segment === 'about' ? 'active' : undefined} href="about">about</NavLink>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
	<a rel=prefetch slot="left" class="{segment === 'blog' ? 'active' : undefined}" href="blog">blog</a>
</Navbar>
