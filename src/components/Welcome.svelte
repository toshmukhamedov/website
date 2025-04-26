<script lang="ts">
	import AboutMe from './AboutMe.svelte';
	import Card from './Card.svelte';
	let isMemojiLoaded = $state(false);

	const onMemojiLoad = () => {
		isMemojiLoaded = true;
	};
</script>

<Card>
	<div class="flex">
		<div class="flex w-3/5 flex-col gap-4">
			<p class="text-lg font-thin">Welcome to my digital space</p>
			<hr class="hr" />
			<AboutMe />
		</div>
		<div class="w-2/5">
			<enhanced:img
				onload={onMemojiLoad}
				class="transition-opacity duration-500 ease-in-out"
				class:opacity-0={!isMemojiLoaded}
				class:opacity-100={isMemojiLoaded}
				alt="memoji"
				src="../lib/assets/memoji.png"
			></enhanced:img>
		</div>
	</div>
</Card>
