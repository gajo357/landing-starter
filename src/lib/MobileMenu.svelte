<script>
	export let isOpen = false;
</script>

<!-- Mobile menu, show/hide based on menu state. -->
{#if isOpen}
	<div class="sm:hidden" id="mobile-menu">
		<div class="space-y-1 px-2 pt-2 pb-3">
			<a
				href="/"
				class="btn-primary block px-3 py-2 rounded-md text-base font-medium"
				aria-current="page">Home</a
			>

			<a href="/about" class="btn-primary block px-3 py-2 rounded-md text-base font-medium">About</a
			>
		</div>
	</div>
{/if}
