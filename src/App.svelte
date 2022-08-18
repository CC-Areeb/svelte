<script>
	import Modal from "./Modal.svelte";
</script>

<!-- a svelte component -->
<Modal />

<main>
	<p>
		Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero rem cumque
		eaque ea facere vel ut temporibus accusantium maxime? Praesentium rerum,
		animi similique delectus eveniet veniam soluta aperiam doloremque
		molestias ipsam corrupti est voluptas non quasi ducimus libero fuga at
		iure nostrum repudiandae sequi. Ipsa dicta debitis minus explicabo
		voluptatem assumenda rem id molestias nam quas, quis asperiores
		perspiciatis veritatis recusandae quae sed minima aspernatur culpa optio
		quisquam aut. Provident explicabo voluptas in tempore incidunt eius
		eligendi dolorem commodi, esse iste repudiandae distinctio dignissimos
		maiores voluptatibus molestiae necessitatibus id autem, aspernatur alias
		dolor? Voluptatum ab corrupti consequatur, odit corporis distinctio?
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
