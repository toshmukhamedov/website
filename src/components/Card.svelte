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
    p-6
    transition-colors
    hover:border-neutral-700
 "
>
	{@render children()}
</div>
