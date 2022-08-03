<script>
	let name = 'Yoshi';
	let beltColor = 'black';

	const changeColor = () => {
		beltColor = 'aqua'
	}
</script>

<main>
	<h1>
		Hello {name}!
	</h1>
	<p>
		I am Learning Svelte :)
	</p>

	<p>
		{beltColor} belt :)
	</p>

	<p>
		To change belt color please press this button <button on:click="{changeColor}">Change color</button>
	</p>

	<p>
		for docs, <a href="https://svelte.dev/tutorial/basics" target="__blank">click me!</a>
	</p>
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