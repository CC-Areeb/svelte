<script>
	let name = 'Yoshi';
	let beltColor = 'orange';

	const changeColor = () => {
		beltColor = 'red'
	}

	/** 
	 * @param event
	 * when we want an event like something happening on a button click then
	 * we pass a parameter inside the function to fire the event
	 */
	const typeColor = (event) => {
		beltColor = event.target.value;
	}
</script>

<main>
	<h1>
		Hello {name}!
	</h1>

	<!-- 
		we can dynamically change colors by asking users to write their colors 
	-->

	<p style="color: {beltColor}">
		{beltColor}
	</p>

	<!-- 
		by using the value attribute, we are binding this input with the default color we had defined in the code
	-->

	<p>
		To change belt color please press this button <br><br> <button on:click="{changeColor}">Change color</button>
		<!--
			this is long way for 2 way binding and we will use a shorthand for 2 way binding
			for 1 way data binding use the long way
			<input type="text" value="{beltColor}" on:input="{typeColor}"> 
		-->

		<input type="text" bind:value={beltColor}>
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