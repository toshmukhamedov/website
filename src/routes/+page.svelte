<script lang="ts">
	import Contact from '$components/Contact.svelte';
	import Socials from '$components/Socials.svelte';
	import Welcome from '$components/Welcome.svelte';
</script>

<div class="mx-8 my-6 flex flex-col gap-4 md:mx-26 md:my-10 md:gap-5 lg:mx-52 lg:my-14 xl:flex-row">
	<div class="xl:w-2/3">
		<Welcome />
	</div>
	<div class="flex flex-col gap-4 md:gap-5 xl:w-1/3">
		<Contact />
		<Socials />
	</div>
</div>
