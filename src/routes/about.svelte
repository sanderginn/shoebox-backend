<script>
	import Button from 'sveltestrap/src/Button.svelte';
	import Form from 'sveltestrap/src/Form.svelte';
	import FormGroup from 'sveltestrap/src/FormGroup.svelte';
	import Label from 'sveltestrap/src/Label.svelte';
	import Input from 'sveltestrap/src/Input.svelte';
	import InputGroup from 'sveltestrap/src/InputGroup.svelte';
	import InputGroupText from 'sveltestrap/src/InputGroupText.svelte';
	import InputGroupAddon from 'sveltestrap/src/InputGroupAddon.svelte';

	function addField() {
		console.log('adding field')
		fields = [...fields, {
			id: fields.length + 1,
			label: "Click to set key",
			editing: false,
			value: null,
			commit: false
		}]
	}

	let fields = []
</script>

<svelte:head>
	<title>Add note</title>
</svelte:head>

<h1>Add a note</h1>

<Button primary on:click={addField}>Add field</Button>
<Form>
{#each fields as field (field.id)}
	<FormGroup>
		{#if !field.editing}
			<Label for={field.id} on:click={console.log("CLicked!")}>{field.label}</Label>
		{:else}
			<InputGroup>
				<InputGroupText placeholder="Enter key"/>
				<InputGroupAddon append></InputGroupAddon>
				<Button class="fas fa-check"/>
				<Button class="fas fa-times"/>
			</InputGroup>
		{/if}
		<Input value={field.value}/>
	</FormGroup>
{/each}
<FormGroup>
	<Label for="note">Note</Label>
	<Input type="textarea" id="note" />
</FormGroup>
</Form>