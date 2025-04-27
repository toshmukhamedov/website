<script lang="ts">
	import Card from './Card.svelte';
	import { HugeiconsIcon } from '@hugeicons/svelte';
	import { MailIcon } from '@hugeicons/core-free-icons';
	import { onMount } from 'svelte';

	let iconsVisible = $state(false);
	const mail = 'a.toshmukhamedov@icould.com';

	onMount(() => {
		setTimeout(() => {
			iconsVisible = true;
		}, 100);
	});
</script>

<Card>
	<h2 class="mb-2 text-sm md:mb-4 lg:text-lg">Contact</h2>
	<ul class="gap-1 md:gap-2">
		<li class="flex items-center gap-1 text-xs font-thin md:gap-1.5 lg:text-base">
			<div
				class="transition-opacity duration-300"
				class:opacity-0={!iconsVisible}
				class:opacity-100={iconsVisible}
			>
				<HugeiconsIcon icon={MailIcon} size={20} />
			</div>
			<a href="mailto:{mail}" class="hover:underline">{mail}</a>
		</li>
	</ul>
</Card>
