<script>
	
	import Modal from './Modal.svelte';

	let showModal = false;

	const toggleModal = () =>{
		showModal = !showModal;
	}
</script>

<Modal {showModal} isPromo={true} on:click={toggleModal}>

<form>
	<h2>Fill up the form below</h2>
	
	<input type="text" placeholder="Your Name"/>
	<input type="text" placeholder="Your Email"/>
	<button>Submit</button>
</form>

<!--<div slot="heading">
	<h2>Fill up the form below</h2>
</div> -->
</Modal>

<main>
	<button on:click={toggleModal}>
		Click to show Modal
	</button>
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