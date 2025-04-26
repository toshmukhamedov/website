<script lang="ts">
	import Card from './Card.svelte';
	import { HugeiconsIcon, type IconSvgElement } from '@hugeicons/svelte';
	import { GithubIcon, LinkedinIcon, DiscordIcon } from '@hugeicons/core-free-icons';

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
</script>

<Card>
	<h2 class="mb-4 text-lg">Socials</h2>
	<ul>
		{#each socials as social, i (i)}
			<li class="my-2 flex items-center gap-1 font-thin">
				<HugeiconsIcon icon={social.icon} />
				<a href={social.url} class="hover:underline" target="_blank">{social.title}</a>
			</li>
		{/each}
	</ul>
</Card>
