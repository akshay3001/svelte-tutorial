<script>
	const num = 10;
	let users = [];
	// let users = [
	// 	{name: 'John', id: 1},
	// 	{name: 'Doe', id: 2},
	// 	{name: 'David', id: 3},
	// ]
</script>

<main>
	{#if num === 0}
		 <h2>Number is 0</h2>
		 {:else if  num < 0}
			  <h2>Number is less than 0</h2>
				{:else if num > 0}
					<h2>Number is greater than 0</h2>
					{:else}
						<h2>Is not a number</h2>
	{/if}
	<hr>

	{#if users.length}
			<h2>List of Users:</h2>
			<ul>
				{#each users as user}
				 	<li>{user.name}</li>
				{/each}
			</ul>
			{:else}
				<h2>No users found</h2>
	{/if}
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