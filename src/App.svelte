<script>
	import Modal from "./Modal.svelte";
	import AddPersonForm from "./AddPersonForm.svelte";

	let ModalShow = false;

	let people = [];

	const deleteButton = (id) => {
		people = people.filter((person) => person.id != id);
	}

	const openModal = () => {
		ModalShow = !ModalShow;
	}

	const addPerson = (event) =>{
		const person = event.detail;
		people = [person, ...people];
		ModalShow = false;
	}
</script>



<Modal isPromo = {true} {ModalShow} on:click={openModal}>
	<AddPersonForm on:addPerson={addPerson} />
</Modal>



<main>
	{#each people as person (person.id)}
		<div>
			<h1 id="person_name">{person.name}</h1>

			<p id="person_belt-color">
				Belt color: {person.belt_color}
			</p>

			<p id="person_age">
				Age: {person.age}
			</p>

			<h5 class="person_weapon">
				Choice of weapon : {person.weapon}
			</h5>

			<button on:click={ ()=> deleteButton(person.id) }>Delete</button>
		</div>
		{:else}
			<h1 id="no_data">
				We have no data here ... (!-_-)
			</h1>

			<p id="add_new_data_text">
				click the button below to add new data (!-_-)
			</p>

			<h5 id="down_arrow">
				&downarrow;
			</h5>
	{/each}
	<button on:click={openModal}>Click me!</button>
</main>

<style>	
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}

	#no_data
	{
		font-size: 5rem;
		color: darkcyan;
	}

	#add_new_data_text
	{
		font-size: 2rem;
	}

	#down_arrow
	{
		font-size: 6rem;
		margin: 0;
	}
</style>
