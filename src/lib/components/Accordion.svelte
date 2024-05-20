<script>
	import { slide } from 'svelte/transition';
	import DownArrow from "$lib/assets/keyboard_down_arrow.svg";
	import UpArrow from "$lib/assets/keyboard_up_arrow.svg";

	export let isOpen = false;
	const handleClick = () => isOpen = !isOpen;

	$: dropDownImageSrc = isOpen ? DownArrow : UpArrow;
</script>

<div on:click={handleClick} role="button" tabindex="0" {...$$restProps}>
	<div class="header">
		<slot name="header" />
		<img src={dropDownImageSrc} alt="Navbar dropdown arrow icon">
	</div>

	{#if isOpen}
	<div class="content" transition:slide>
		<slot name="content">
		</slot>
	</div>
	{/if}
</div>

<!-- Minimal styling to allow customiseability -->
<style>
	div.header {
		display: flex;
		justify-content: space-between;
	}
</style>
