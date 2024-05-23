<script>
	import { DarkMode, Navbar, NavBrand } from 'flowbite-svelte';
</script>

<Navbar class="fixed start-0 top-0 z-20 w-full border-b">
	<NavBrand href="/">
		<span class="self-center whitespace-nowrap text-xl font-semibold">Sp1ke TODO</span>
	</NavBrand>
	<div class="ml-auto flex items-center">
		<DarkMode class="inline-block hover:text-gray-900 dark:hover:text-white" />
	</div>
</Navbar>

<style>
</style>
