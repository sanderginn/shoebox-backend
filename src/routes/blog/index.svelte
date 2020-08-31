<script context="module">
	 import Card from 'sveltestrap/src/Card.svelte';
	 import CardHeader from 'sveltestrap/src/CardHeader.svelte';
	 import CardTitle from 'sveltestrap/src/CardTitle.svelte';
	 import Button from 'sveltestrap/src/Button.svelte';
</script>


<svelte:head>
	<title>Chota</title>
</svelte:head>

<h1>Chota test</h1>

<Card>
	<CardHeader>
		<CardTitle>Card title</CardTitle>
	</CardHeader>
	A nisi ullam impedit molestiae, sapiente id, 
	numquam accusantium eius cum, iste eum iusto 
	blanditiis doloribus beatae. 
	Molestias iste explicabo libero nam, 
	voluptas harum ipsum quod velit enim. 
	Quae, cupiditate?
	
	<div slot="footer" class="is-right">
			<Button danger>Cancel</Button>
			<Button primary>Confirm</Button>
	</div>
</Card>