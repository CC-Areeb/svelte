<script>
	import Modal from "./Modal.svelte";

	let ModalShow = false;

	const openModal = () => {
		ModalShow = !ModalShow;
	}
</script>



<!-- a svelte component -->
<Modal
offer = "Limited time offer"
price = 20
isPromo = {true}
{ModalShow}
on:click={openModal} 
/>



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
