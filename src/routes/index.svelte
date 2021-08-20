<script lang="ts">
	import { onMount } from 'svelte';
	import Link from '$lib/Link.svelte';
	import Laptop from '$lib/Laptop.svelte';

	let animate = false;

	onMount(() => (animate = true));
</script>

<section class="col-span-12 h-full flex flex-col justify-center items-center">
	<h1 class="title text-4xl text-blueGray-700 mb-8">Ivan Wang</h1>
	<ul class="grid grid-flow-row gap-y-4 tracking-widest sm:grid-flow-col sm:gap-x-16">
		<li class="flex justify-center">
			<Link path="/about" label="about" />
		</li>
		<li class="flex justify-center">
			<Link path="/projects" label="projects" />
		</li>
		<li class="flex justify-center">
			<Link path="/resume" label="resume" />
		</li>
	</ul>

	{#if animate}
		<Laptop />
	{/if}

	<!-- <div class="relative w-96 h-48 mt-16">
		<img src="res/laptop.svg" class="absolute w-full h-full" alt="laptop" />
		<img src="res/pad.svg" class="absolute right-2 top-12" width="128" height="128" alt="pad" />
		<img src="res/mouse.svg" class="absolute right-10 top-16" width="64" height="64" alt="mouse" />
		<img src="res/plant.svg" class="absolute left-8 bottom-0" width="64" height="64" alt="plant" />
	</div> -->
</section>
