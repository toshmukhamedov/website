<script lang="ts">
	import AboutMe from './AboutMe.svelte';
	import Card from './Card.svelte';
	let isMemojiLoaded = $state(false);

	const onMemojiLoad = () => {
		isMemojiLoaded = true;
	};
</script>

<Card>
	<p class="mb-2 text-sm font-thin lg:mb-4 lg:text-lg">Welcome to my digital space</p>
	<hr class="hr md:mb-2 lg:mb-4" />
	<div class="flex flex-col-reverse items-center md:flex-row md:items-start">
		<div class="md:w-3/5">
			<AboutMe />
		</div>
		<div class="w-3/5 md:flex md:w-2/5 md:items-end md:justify-end">
			<enhanced:img
				onload={onMemojiLoad}
				class="transition-opacity duration-700 ease-in-out"
				class:opacity-0={!isMemojiLoaded}
				class:opacity-100={isMemojiLoaded}
				alt="memoji"
				src="../lib/assets/memoji.png"
			></enhanced:img>
		</div>
	</div>
</Card>
