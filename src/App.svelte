<script>
	import Library from "./library/Library.svelte"

	function handleBookSelect(event) {
		console.log('>>> id: ', event.detail.id)
	}
</script>

<main>
	<Library on:book-select={handleBookSelect} />
</main>

<style>
	
</style>