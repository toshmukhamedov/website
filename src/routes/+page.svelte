<script lang="ts">
	import Contact from '$components/Contact.svelte';
	import Socials from '$components/Socials.svelte';
	import Welcome from '$components/Welcome.svelte';
</script>

<div class="mx-52 my-14 flex gap-4">
	<div class="w-2/3">
		<Welcome />
	</div>
	<div class="flex w-1/3 flex-col gap-4">
		<Contact />
		<Socials />
	</div>
</div>
