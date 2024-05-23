<script>
	import '../app.css';
	import Bottombar from '$lib/Bottombar.svelte';
	import Menubar from '$lib/Menubar.svelte';
	import Topbar from '$lib/Topbar.svelte';
</script>

<div class="container p-2 lg:p-6">
	<Topbar />

	<div class="mx-auto flex w-full px-4 pt-16">
		<Menubar />

		<main class="mx-auto w-full lg:ml-32">
			<slot />
		</main>
	</div>

	<Bottombar />
</div>

<style></style>
