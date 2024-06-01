<script lang="ts">
	import { BottomNav, BottomNavItem, Tooltip } from 'flowbite-svelte';
	import { GithubSolid, GoogleSolid, LinkedinSolid, UserCircleSolid } from 'flowbite-svelte-icons';

	let navigateTo = (url: string) => {
		window.open(url, '_blank');
	};
</script>

<BottomNav position="absolute" navType="application" classInner="grid-cols-4">
	<BottomNavItem btnName="Github" appBtnPosition="left" on:click={() => navigateTo('https://github.com/h4j4x')}>
		<GithubSolid
			class="mb-1 h-6 w-6 text-gray-500 group-hover:text-primary-600 dark:text-gray-400 dark:group-hover:text-primary-500"
		/>
		<Tooltip arrow={false}>GitHub</Tooltip>
	</BottomNavItem>
	<BottomNavItem btnName="Linkedin" appBtnPosition="middle" on:click={() => navigateTo('https://www.linkedin.com/in/h4j4x/')}>
		<LinkedinSolid
			class="mb-1 h-6 w-6 text-gray-500 group-hover:text-primary-600 dark:text-gray-400 dark:group-hover:text-primary-500"
		/>
		<Tooltip arrow={false}>Linkedin</Tooltip>
	</BottomNavItem>
	<BottomNavItem btnName="Google Developer" appBtnPosition="middle" on:click={() => navigateTo('https://g.dev/sp1ke')}>
		<GoogleSolid
			class="mb-1 h-6 w-6 text-gray-500 group-hover:text-primary-600 dark:text-gray-400 dark:group-hover:text-primary-500"
		/>
		<Tooltip arrow={false}>Google Developer</Tooltip>
	</BottomNavItem>
	<BottomNavItem btnName="Profile" appBtnPosition="right">
		<UserCircleSolid
			class="mb-1 h-6 w-6 text-gray-500 group-hover:text-primary-600 dark:text-gray-400 dark:group-hover:text-primary-500"
		/>
		<Tooltip arrow={false}>Profile</Tooltip>
	</BottomNavItem>
</BottomNav>

<style></style>
