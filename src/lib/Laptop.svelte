<script lang="ts">
	import { fly } from 'svelte/transition';
</script>

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
