<script>
	import Library from "./library/Library.svelte"

	function handleBookSelect(id) {
		console.log('>>> id: ', id)
	}
</script>

<main>
	<Library onBookSelect={handleBookSelect} />
</main>

<style>
	
</style>