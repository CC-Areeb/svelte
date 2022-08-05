<script>
	let items = [
		{name: 'Yoshi', belt_color: 'black', age: '28', id: '1'},
		{name: 'Mario', belt_color: 'orange', age: '28', id: '2'},
		{name: 'Luigi', belt_color: 'red', age: '28', id: '3'},
		{name: 'Toad', belt_color: 'yellow', age: '28', id: '4'}
	];
</script>

<main>
	<!-- we will use a loop to cycle and display the array data -->
	{#each items as item (items.id)}
		<!-- now we difine the html template for the output -->
		<div>
			<h1>{item.name}</h1>
			<p>
				Belt color is {item.belt_color} and I am {item.age} years old
			</p>
		</div>
		{:else}
			<!-- else content here -->
			<p>
				We have no data here ... (!-_-)
			</p>
	{/each}
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