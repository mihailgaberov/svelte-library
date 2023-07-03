<script>
	import Details from "./library/Details.svelte";
import Library from "./library/Library.svelte"


	let page = 'library'
	let pageArgs = {}


	function handleBookSelect(event) {
		page = 'detail'
		pageArgs = event.detail
	}
</script>

<main>
	{#if page === 'detail'}
		<Details {...pageArgs} />
		{:else}
		<Library on:book-select={handleBookSelect} />
	{/if}
	
</main>

<style>
	main {
		padding: var(--spacingLarge);
	}
</style>