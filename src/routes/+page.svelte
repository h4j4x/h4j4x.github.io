<script lang="ts">
	import { Timeline, TimelineItem, Button } from 'flowbite-svelte';
	import { ArrowRightOutline, CalendarWeekSolid } from 'flowbite-svelte-icons';

	interface TimelineType {
		title: string;
		date: string;
		description: string;
		hasLearnMore: boolean;
	}

	let items: Array<TimelineType> = [
		{
			title: 'Application UI code in Tailwind CSS',
			date: 'February 2022',
			description:
				'Get access to over 20+ pages including a dashboard layout, charts, kanban board, calendar, and pre-order E-commerce & Marketing pages.',
			hasLearnMore: true
		},
		{
			title: 'Application UI code in Tailwind CSS',
			date: 'March 2022',
			description:
				'All of the pages and components are first designed in Figma and we keep a parity between the two versions even as we update the project.',
			hasLearnMore: false
		},
		{
			title: 'Application UI code in Tailwind CSS',
			date: 'April 2022',
			description: 'Get started with dozens of web components and interactive elements built on top of Tailwind CSS.',
			hasLearnMore: false
		},
		{
			title: 'Application UI code in Tailwind CSS',
			date: 'February 2022',
			description:
				'Get access to over 20+ pages including a dashboard layout, charts, kanban board, calendar, and pre-order E-commerce & Marketing pages.',
			hasLearnMore: true
		},
		{
			title: 'Application UI code in Tailwind CSS',
			date: 'March 2022',
			description:
				'All of the pages and components are first designed in Figma and we keep a parity between the two versions even as we update the project.',
			hasLearnMore: false
		},
		{
			title: 'Application UI code in Tailwind CSS',
			date: 'April 2022',
			description: 'Get started with dozens of web components and interactive elements built on top of Tailwind CSS.',
			hasLearnMore: false
		}
	];
</script>

<div class="max-h-[calc(100vh_-_12rem)] overflow-y-scroll overflow-x-clip px-10">
	<Timeline order="vertical">
		{#each items as item, i (i)}
			<TimelineItem title={item.title} date={item.date}>
				<svelte:fragment slot="icon">
					<span
						class="absolute -start-3 flex h-6 w-6 items-center justify-center rounded-full bg-primary-200 dark:bg-primary-900"
					>
						<CalendarWeekSolid class="h-5 w-5 text-primary-600 dark:text-primary-400" />
					</span>
				</svelte:fragment>
				<p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">
					{item.description}
				</p>
				{#if item.hasLearnMore}
					<Button color="alternative">Learn more<ArrowRightOutline class="ms-2 h-5 w-5" /></Button>
				{/if}
			</TimelineItem>
		{/each}
	</Timeline>
</div>
