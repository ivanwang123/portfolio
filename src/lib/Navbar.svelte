<script lang="ts">
	import { page } from '$app/stores';
	import { slide } from 'svelte/transition';
	import Link from '$lib/Link.svelte';
	import Hamburger from '$lib/assets/hamburger.svg?component';
	import ArrowUp from '$lib/assets/arrow-up.svg?component';

	let showMenu = false;
	let menuBtn;

	type NavLink = {
		path: string;
		label: string;
		selected: boolean;
	};

	let navLinks: NavLink[];
	$: {
		navLinks = [
			{ path: '/about', label: 'about', selected: $page.path === '/about' },
			{ path: '/projects', label: 'projects', selected: $page.path === '/projects' },
			{ path: '/resume', label: 'resume', selected: $page.path === '/resume' }
		];
	}

	console.log($page.path);

	const toggleMenu = () => {
		showMenu = !showMenu;
	};
</script>

<nav class="grid grid-cols-12 py-6">
	<div class="col-start-1 col-end-13 flex items-center px-4 sm:col-start-2 sm:col-end-12 sm:px-0">
		<h3 class="text-xl text-blueGray-800 font-semibold">
			<a sveltekit:prefetch href="/">Ivan Wang</a>
		</h3>
		<div class="ml-auto sm:hidden">
			<button type="button" on:click={toggleMenu} bind:this={menuBtn}>
				<Hamburger class="w-5 h-5 pointer-events-none" />
			</button>
			{#if showMenu}
				<div class="fixed inset-0 h-full flex flex-col items-center bg-white" transition:slide>
					<h1 class="text-2xl text-blueGray-800 font-semibold mb-8 mt-auto">Ivan Wang</h1>
					<ul class="grid grid-flow-row gap-y-4 mb-auto">
						{#each navLinks as link (link)}
							<li
								class={`flex justify-center ${link.selected && 'bg-blue-50'}`}
								on:click={toggleMenu}
							>
								<Link path={link.path} label={link.label} />
							</li>
						{/each}
					</ul>
					<div class="text-gray-300 mb-10 cursor-pointer" on:click={toggleMenu}>
						<ArrowUp class="w-12 h-12 fill-current" />
					</div>
				</div>
			{/if}
		</div>

		<ul class="hidden grid-flow-col gap-x-8 ml-auto sm:grid">
			{#each navLinks as link (link)}
				<li class={`flex justify-center ${link.selected && 'bg-blue-50'}`}>
					<Link path={link.path} label={link.label} />
				</li>
			{/each}
		</ul>
	</div>
</nav>
