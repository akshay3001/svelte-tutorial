<script>
	const name = 'Test';
	const test1 = 'Test1';
	const test2 = 'Test2';
	const test3 = 'Test3';
</script>

<main>
	<h1>Hello {name}!</h1>
	<h1>{test1}!</h1>
	<h1>{test2}!</h1>
	<h1>{test3}!</h1>
	<h1>{8*8}!</h1>
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