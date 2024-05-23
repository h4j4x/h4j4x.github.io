<script>
	import { BottomNav, BottomNavItem, Tooltip } from 'flowbite-svelte';
	import {
		GithubSolid,
		LinkedinSolid,
		AdjustmentsVerticalOutline,
		UserCircleSolid,
	} from 'flowbite-svelte-icons';
</script>

<BottomNav position="absolute" navType="application" classInner="grid-cols-4">
	<BottomNavItem btnName="Github" appBtnPosition="left">
		<GithubSolid
			class="mb-1 h-6 w-6 text-gray-500 group-hover:text-primary-600 dark:text-gray-400 dark:group-hover:text-primary-500"
		/>
		<Tooltip arrow={false}>GitHub</Tooltip>
	</BottomNavItem>
	<BottomNavItem btnName="Linkedin" appBtnPosition="middle">
		<LinkedinSolid
			class="mb-1 h-6 w-6 text-gray-500 group-hover:text-primary-600 dark:text-gray-400 dark:group-hover:text-primary-500"
		/>
		<Tooltip arrow={false}>Linkedin</Tooltip>
	</BottomNavItem>
	<BottomNavItem btnName="Settings" appBtnPosition="middle">
		<AdjustmentsVerticalOutline
			class="mb-1 h-6 w-6 text-gray-500 group-hover:text-primary-600 dark:text-gray-400 dark:group-hover:text-primary-500"
		/>
		<Tooltip arrow={false}>Settings</Tooltip>
	</BottomNavItem>
	<BottomNavItem btnName="Profile" appBtnPosition="right">
		<UserCircleSolid
			class="mb-1 h-6 w-6 text-gray-500 group-hover:text-primary-600 dark:text-gray-400 dark:group-hover:text-primary-500"
		/>
		<Tooltip arrow={false}>Profile</Tooltip>
	</BottomNavItem>
</BottomNav>

<style></style>
