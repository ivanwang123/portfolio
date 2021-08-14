<script lang="ts">
	import { onMount } from 'svelte';
	import { fly } from 'svelte/transition';

	let animate = false;

	onMount(() => (animate = true));
</script>

<section class="col-span-12 h-full flex flex-col justify-center items-center">
	<h1 class="text-4xl mb-8">Ivan Wang</h1>
	<ul class="grid grid-flow-row gap-y-4 tracking-widest sm:grid-flow-col sm:gap-x-16">
		<li class="flex justify-center"><a sveltekit:prefetch href="/about">about</a></li>
		<li class="flex justify-center"><a sveltekit:prefetch href="/projects">projects</a></li>
		<li class="flex justify-center"><a sveltekit:prefetch href="/resume">resume</a></li>
	</ul>

	{#if animate}
		<div class="relative w-72 h-36 mt-16">
			<img
				src="res/laptop.svg"
				class="absolute w-full h-full"
				in:fly={{ y: -50, duration: 600, delay: 100 }}
				alt="laptop"
			/>
			<img
				src="res/pad.svg"
				class="absolute right-1 top-8"
				in:fly={{ y: -50, duration: 600, delay: 200 }}
				width="100"
				height="100"
				alt="pad"
			/>
			<img
				src="res/mouse.svg"
				class="absolute right-6 top-11"
				in:fly={{ y: -50, duration: 600, delay: 300 }}
				width="56"
				height="56"
				alt="mouse"
			/>
			<img
				src="res/plant.svg"
				class="absolute left-4 bottom-0"
				in:fly={{ y: -50, duration: 600, delay: 0 }}
				width="56"
				height="56"
				alt="plant"
			/>
		</div>
	{/if}

	<!-- <div class="relative w-96 h-48 mt-16">
		<img src="res/laptop.svg" class="absolute w-full h-full" alt="laptop" />
		<img src="res/pad.svg" class="absolute right-2 top-12" width="128" height="128" alt="pad" />
		<img src="res/mouse.svg" class="absolute right-10 top-16" width="64" height="64" alt="mouse" />
		<img src="res/plant.svg" class="absolute left-8 bottom-0" width="64" height="64" alt="plant" />
	</div> -->
</section>
