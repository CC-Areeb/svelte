<script>
	import Modal from "./Modal.svelte";
	import AddPersonForm from "./AddPersonForm.svelte";

	let ModalShow = false;

	const openModal = () => {
		ModalShow = !ModalShow;
	}
</script>



<!-- a svelte component -->
<Modal isPromo = {true} {ModalShow} on:click={openModal}>
	<AddPersonForm/>
</Modal>



<main>
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
</style>
