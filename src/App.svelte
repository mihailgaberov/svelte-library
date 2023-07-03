<script>
	import { Route, Router } from "svelte-routing";

	import Details from "./library/Details.svelte";
	import Library from "./library/Library.svelte";

	export let url = "";
</script>

<Router {url}>
	<main>
		<Route path="/books/:id" let:params>
			<Details id={params.id} />
		</Route>
		<Route path="/">
			<Library />
		</Route>
	</main>
</Router>

<style>
	main {
		padding: var(--spacingLarge);
	}
</style>
