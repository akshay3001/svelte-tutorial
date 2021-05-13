<script>
	const name = 'Test';
	const success = 'success';
	const isSelected = true;
</script>

<main>
	<h1>Hello {name}!</h1>
	<h2 class='primary'>Primary</h2>
	<h2 class={success}>Success</h2>
	<h2 class={isSelected ? 'isSelected' : ''}>Selected</h2>
	Since both the condition variable and class names are same Svelte has a syntax for it:
	<h2 class:isSelected>Selected</h2>
</main>

<style>
	.primary {
		color: blue;
	}

	.success {
		color: green;
	}

	.isSelected {
		color: yellow;
	}

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