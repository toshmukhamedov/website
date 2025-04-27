<script lang="ts">
	let { children } = $props();
</script>

<div
	class="
	  card
	  rounded-lg
	  border
	  border-neutral-800
	  bg-neutral-900
		p-4
		transition-colors
		hover:border-neutral-700
    md:p-5
    lg:p-6
 "
>
	{@render children()}
</div>
