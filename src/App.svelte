<script>
	let items = [
		{name: 'Yoshi', belt_color: 'black', age: '28', id: '1'},
		{name: 'Mario', belt_color: 'orange', age: '28', id: '2'},
		{name: 'Luigi', belt_color: 'red', age: '28', id: '3'},
		{name: 'Toad', belt_color: 'yellow', age: '28', id: '4'}
	];


	const deleteButton = (id) => {
		// deleting a record
		// we will fire a callback function
		items = items.filter((item) => item.id != id);
	}

	let test_number = 5;
</script>

<main>
{#each items as item (item.id) }
	<div>
		<h1>{item.name}</h1>

		{#if item.belt_color === 'black'}
			<p>I am Yoshi</p>

		{:else if item.belt_color === 'orange'}
			<p>I am Mario</p>

		{:else if item.belt_color === 'red'}
			<p>I am Luigi</p>

		{:else if item.belt_color === 'yellow'}
			<p>I am Toad</p>

			{:else}
			<p>Oops .... we don't have that color</p>
		{/if}

		<p>Belt color is {item.belt_color}</p>
		<h5>Age: {item.age}</h5>
		<button on:click={ ()=> deleteButton(item.id) }>Delete</button>
	</div>
{:else}
	<h1>No data!!!</h1>
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