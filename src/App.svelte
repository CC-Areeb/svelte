<script>
	import Modal from "./Modal.svelte";

	let ModalShow = false;

	const openModal = () => {
		ModalShow = !ModalShow;
	}
</script>



<!-- a svelte component -->
<Modal isPromo = {true} {ModalShow} on:click={openModal}>
	<h3 slot="title">
		Add a new person
	</h3>

	<form class="modal-form">
		<input type="text" name="name" id="name" placeholder="Name">
		<input type="text" name="belt_color" id="belt_color" placeholder="Belt color">
		<button>Add person</button>
	</form>
</Modal>



<main>
	<button on:click={openModal}>Click me!</button>
</main>

<style>

	.modal-form
	{
		display: flex;
		flex-direction: column;
	}

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
</style>
