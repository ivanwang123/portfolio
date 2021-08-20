<script lang="ts">
	import { slide } from 'svelte/transition';
	import Link from '$lib/Link.svelte';
	import Hamburger from '$lib/assets/hamburger.svg?component';

	let showMenu = false;
	let menuBtn;

	const navLinks = ['about', 'projects', 'resume'];

	const toggleMenu = () => {
		showMenu = !showMenu;
	};
</script>

<nav class="grid grid-cols-12 py-6">
	<div class="col-start-1 col-end-13 flex items-center px-4 sm:col-start-2 sm:col-end-12 sm:px-0">
		<h3 class="text-xl"><a sveltekit:prefetch href="/">Ivan Wang</a></h3>
		<div class="ml-auto sm:hidden">
			<button type="button" on:click={toggleMenu} bind:this={menuBtn}>
				<Hamburger class="w-5 h-5 pointer-events-none" />
			</button>
			{#if showMenu}
				<div
					class="fixed inset-0 flex flex-col justify-center items-center bg-white"
					transition:slide
				>
					<h1 class="text-3xl mb-8">Ivan Wang</h1>
					<ul class="grid grid-flow-row gap-y-4">
						{#each navLinks as link (link)}
							<li class="flex justify-center" on:click={toggleMenu}>
								<Link path={link} label={link} />
							</li>
						{/each}
					</ul>
				</div>
			{/if}
		</div>

		<ul class="hidden grid-flow-col gap-x-8 ml-auto sm:grid">
			{#each navLinks as link (link)}
				<li class="flex justify-center">
					<Link path={link} label={link} />
				</li>
			{/each}
		</ul>
	</div>
</nav>
