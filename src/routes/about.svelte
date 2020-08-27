<script>
	function addField() {
		console.log('adding field')
		fields = [...fields, {
			label: "Click to set label",
			value: null,
			commit: false
		}]
	}

	import {Field,Input,Button} from 'svelte-chota';

	let fields = []
</script>

<svelte:head>
	<title>Add note</title>
</svelte:head>

<h1>Add a note</h1>

<Button primary on:click={addField}>Add field</Button>
{#each fields as field}
	<Field label={field.label}>
		<p><Input value={field.value}/></p>
	</Field>
{/each}
<Field label="Note">
	<p><Input textarea/></p>
</Field>