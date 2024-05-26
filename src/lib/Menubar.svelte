<script lang="ts">
	import { Sidebar, SidebarGroup, SidebarItem, SidebarWrapper } from 'flowbite-svelte';
	import {
		ChartPieSolid,
		GridSolid,
		MailBoxSolid,
		UserSolid,
		ShoppingBagSolid,
		ArrowRightToBracketOutline,
		EditOutline,
		FireSolid,
		BookSolid,
		RestoreWindowOutline,
		LifeSaverSolid
	} from 'flowbite-svelte-icons';
	import type { ComponentType } from 'svelte';

	let spanClass = 'flex-1 ms-3 whitespace-nowrap';
	let iconClass =
		'h-6 w-6 text-gray-500 transition duration-75 group-hover:text-gray-900 dark:text-gray-400 dark:group-hover:text-white';

	interface MenuItemType {
		label: string;
		icon: ComponentType;
		subtext?: string;
		subtextProps?: Record<string, any>;
	}
	let items: Array<MenuItemType> = [
		{
			label: 'Dashboard',
			icon: ChartPieSolid
		},
		{
			label: 'Kanban',
			icon: GridSolid,
			subtext: 'Pro',
			subtextProps: {
				class:
					'ms-3 inline-flex items-center justify-center rounded-full bg-gray-200 px-2 text-sm font-medium text-gray-800 dark:bg-gray-700 dark:text-gray-300'
			}
		},
		{
			label: 'Inbox',
			icon: MailBoxSolid,
			subtext: '3',
			subtextProps: {
				class:
					'ms-3 inline-flex h-3 w-3 items-center justify-center rounded-full bg-primary-200 p-3 text-sm font-medium text-primary-600 dark:bg-primary-900 dark:text-primary-200'
			}
		},
		{
			label: 'Users',
			icon: UserSolid
		},
		{
			label: 'Products',
			icon: ShoppingBagSolid
		}
	];
</script>

<Sidebar asideClass="w-54 hidden lg:flex">
	<SidebarWrapper>
		<SidebarGroup>
			{#each items as item, i (i)}
				<SidebarItem label={item.label} spanClass={item.icon ? spanClass : undefined}>
					<svelte:fragment slot="icon">
						<svelte:component this={item.icon} class={iconClass} />
					</svelte:fragment>
					<svelte:fragment slot="subtext">
						{#if item.subtext}
							<span {...item.subtextProps}>
								{item.subtext}
							</span>
						{/if}
					</svelte:fragment>
				</SidebarItem>
			{/each}
		</SidebarGroup>
	</SidebarWrapper>
</Sidebar>

<style></style>
