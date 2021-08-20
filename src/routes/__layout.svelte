<script lang="ts">
	import { page } from '$app/stores';
	import Navbar from '$lib/Navbar.svelte';
	import '../app.postcss';

	// const handleClickOutside = (elem) => {
	// 	const onClick = (e) => {
	// 		if (!elem.contains(e.target) && e.target !== menuBtn) {
	// 			showMenu = false;
	// 		}
	// 	};

	// 	document.body.addEventListener('click', onClick);

	// 	return {
	// 		destroy() {
	// 			document.body.removeEventListener('click', onClick);
	// 		}
	// 	};
	// };
</script>

{#if $page.path !== '/'}
	<Navbar />
{/if}

<main class="grid grid-cols-12 w-full h-full">
	<slot />
</main>
