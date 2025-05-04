<script>
	import { HugeiconsIcon } from '@hugeicons/svelte';
	import { Download04Icon } from '@hugeicons/core-free-icons';
</script>

<p class="text-base font-thin">
	I’m <b>Abdugani Toshmukhamedov</b>, a software engineer from Uzbekistan who enjoys contributing
	open-source projects.<br />
	<br />
	Beyond coding, I’m passionate about space, physics, and appreciating the beauty of nature. I’m always
	curious about how everything around us works, from the smallest atoms to the stars.
</p>

<div class="mt-4 flex items-center gap-2">
	<a class="text-sm font-thin underline" href="resume.pdf" target="_blank">View resume</a>
	<a class="text-neutral-400 hover:text-neutral-200" href="resume.pdf" download="Abdugani's resume">
		<HugeiconsIcon icon={Download04Icon} strokeWidth={2} size={20} />
	</a>
</div>
