<script>
	import {Nav} from 'svelte-chota';
	export let segment;
</script>

<Nav>
	<a slot="left" href="/" class="brand">Shoebox</a>
	<a slot="left" class="{segment === undefined ? 'active' : undefined}" href=".">home</a>
	<a slot="left" class="{segment === 'about' ? 'active' : undefined}" href="about">about</a>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
	<a rel=prefetch slot="left" class="{segment === 'blog' ? 'active' : undefined}" href="blog">blog</a>
</Nav>
