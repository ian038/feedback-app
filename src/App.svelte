<script>
	let firstName = 'Ian';
	let lastName = 'Phua'
	let showText = false
	let users = [
		{
			id: '1',
			name: 'John'
		},
		{
			id: '2',
			name: 'Brandon'
		},
		{
			id: '3',
			name: 'Mike'
		}
	]

	const toggle = () => {
		showText = !showText
	}

	$: name = firstName + ' ' + lastName
</script>

<main>
	<h1>Hello {name}!</h1>
	{#if showText}
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	{/if}
	<button on:click={toggle}>Click</button>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>