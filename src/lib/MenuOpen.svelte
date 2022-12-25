<script>
	export let isOpen = false;
</script>

<!--
    Icon when menu is closed.

    Heroicon name: outline/bars-3

    Menu open: "hidden", Menu closed: "block"
-->
<svg
	class={'h-6 w-6' + (isOpen ? ' hidden' : ' block')}
	xmlns="http://www.w3.org/2000/svg"
	fill="none"
	viewBox="0 0 24 24"
	stroke-width="1.5"
	stroke="currentColor"
	aria-hidden="true"
>
	<path
		stroke-linecap="round"
		stroke-linejoin="round"
		d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
	/>
</svg>
<!--
    Icon when menu is open.

    Heroicon name: outline/x-mark

    Menu open: "block", Menu closed: "hidden"
-->
<svg
	class={'h-6 w-6' + (isOpen ? ' block' : ' hidden')}
	xmlns="http://www.w3.org/2000/svg"
	fill="none"
	viewBox="0 0 24 24"
	stroke-width="1.5"
	stroke="currentColor"
	aria-hidden="true"
>
	<path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
</svg>
