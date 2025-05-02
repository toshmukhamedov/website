<script lang="ts">
	import Card from './Card.svelte';
	import { HugeiconsIcon, type IconSvgElement } from '@hugeicons/svelte';
	import { GithubIcon, LinkedinIcon, DiscordIcon } from '@hugeicons/core-free-icons';
	import { onMount } from 'svelte';
	let iconsVisible = $state(false);

	type Social = {
		icon: IconSvgElement;
		title: string;
		url: string;
	};
	const socials: Social[] = [
		{
			icon: GithubIcon,
			title: 'GitHub',
			url: 'https://github.com/toshmukhamedov'
		},
		{
			icon: LinkedinIcon,
			title: 'LinkedIn',
			url: 'https://www.linkedin.com/in/abdugani'
		},
		{
			icon: DiscordIcon,
			title: 'Discord',
			url: 'https://discord.gg/8jAehcAk'
		}
	];

	onMount(() => {
		setTimeout(() => {
			iconsVisible = true;
		}, 100);
	});
</script>

<Card>
	<h2 class="mb-2 text-base lg:mb-4 lg:text-lg">Socials</h2>
	<ul>
		{#each socials as social, i (i)}
			<li class="my-2 flex items-center gap-1 text-base font-thin md:gap-1.5">
				<div
					class="transition-opacity duration-300"
					class:opacity-0={!iconsVisible}
					class:opacity-100={iconsVisible}
				>
					<HugeiconsIcon icon={social.icon} size={20} />
				</div>
				<a href={social.url} class="hover:underline" target="_blank">{social.title}</a>
			</li>
		{/each}
	</ul>
</Card>
