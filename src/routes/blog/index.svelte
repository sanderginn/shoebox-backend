<script context="module">
	import {Card,Button} from 'svelte-chota';
</script>

<svelte:head>
	<title>Chota</title>
</svelte:head>

<h1>Chota test</h1>

<Card>
	<h4 slot="header">Card title</h4>

	A nisi ullam impedit molestiae, sapiente id, 
	numquam accusantium eius cum, iste eum iusto 
	blanditiis doloribus beatae. 
	Molestias iste explicabo libero nam, 
	voluptas harum ipsum quod velit enim. 
	Quae, cupiditate?
	
	<div slot="footer" class="is-right">
			<Button clear>Cancel</Button>
			<Button primary on:click={()=>console.log('Hi!')}>Confirm</Button>
	</div>
</Card>