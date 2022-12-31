<script lang="ts">
	import { createEventDispatcher } from 'svelte';

	export let isOpen = false;
	const dispatch = createEventDispatcher();
	const onClick = () => {
		dispatch('onNavigate', {});
	};
</script>

<!-- Mobile menu, show/hide based on menu state. -->
{#if isOpen}
	<div
		class="sm:hidden absolute left-0 z-10 mt-2 w-48 origin-top-left rounded-md bg-white py-1 shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
		role="menu"
		aria-orientation="vertical"
		aria-labelledby="user-menu-button"
		id="mobile-menu"
	>
		<div class="space-y-1 px-2 pt-2 pb-3">
			<a
				href="/"
				class="block px-3 py-2 rounded-md text-base font-medium"
				aria-current="page"
				on:click={onClick}>Home</a
			>

			<a href="/about" class="px-3 py-2 rounded-md text-base font-medium" on:click={onClick}
				>About</a
			>
		</div>
	</div>
{/if}
