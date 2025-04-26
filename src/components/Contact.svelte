<script lang="ts">
	import Card from './Card.svelte';
	import { HugeiconsIcon } from '@hugeicons/svelte';
	import { MailIcon } from '@hugeicons/core-free-icons';

	const mail = 'a.toshmukhamedov@icould.com';
</script>

<Card>
	<h2 class="mb-4 text-lg">Contact</h2>
	<ul class="gap-2">
		<li class="flex items-center gap-1 font-thin">
			<HugeiconsIcon icon={MailIcon} />
			<a href="mailto:{mail}" class="hover:underline">{mail}</a>
		</li>
	</ul>
</Card>
