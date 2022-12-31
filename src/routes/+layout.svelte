<script>
	import MenuOpen from '$lib/MenuOpen.svelte';
	import MobileMenu from '$lib/MobileMenu.svelte';
	import TabletMenu from '$lib/TabletMenu.svelte';
	import NotificationButton from '$lib/NotificationButton.svelte';
	import ProfileMenu from '$lib/ProfileMenu.svelte';
	import '../app.css';

	let isMenuOpen = false;
</script>

<nav class="bg-white">
	<div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
		<div class="relative flex h-16 items-center justify-between">
			<div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
				<!-- Mobile menu button-->
				<button
					type="button"
					class="inline-flex items-center justify-center rounded-md p-2 btn-primary focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
					aria-controls="mobile-menu"
					aria-expanded="false"
					on:click={() => (isMenuOpen = !isMenuOpen)}
				>
					<MenuOpen isOpen={isMenuOpen} />
				</button>
			</div>

			<TabletMenu />
			<div
				class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0"
			>
				<NotificationButton />

				<ProfileMenu />
			</div>
		</div>
	</div>
	<MobileMenu isOpen={isMenuOpen} on:onNavigate={() => (isMenuOpen = false)} />
</nav>
<div class="text-center">
	<slot />
</div>
