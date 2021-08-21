<script lang="ts">
	import Link from '$lib/assets/link.svg?component';

	export let title: string;
	export let link: string;
	export let tags: string[];
	export let description: string;
</script>

<div class="w-full">
	<div class="border rounded-md overflow-hidden">
		<div class="flex items-center h-7 bg-gray-100 px-4">
			<div class="w-3 h-3 bg-red-400 mr-2 rounded-full" />
			<div class="w-3 h-3 bg-yellow-400 mr-2 rounded-full" />
			<div class="w-3 h-3 bg-green-400 mr-2 rounded-full" />
		</div>
		<img src="res/screenshot1.png" alt="screenshot" />
	</div>
</div>
<div class="mt-3 mb-10 md:mb-14">
	<h3 class="text-xl text-blueGray-800 font-bold">
		<a href={link} rel="noopener noreferrer" target="_blank">{title}</a>
	</h3>
	<a
		class="flex items-center w-max text-gray-400"
		href={link}
		rel="noopener noreferrer"
		target="_blank"
	>
		<Link class="w-4 h-4 fill-current mr-1" />
		{link}
	</a>
	<div class="flex flex-wrap mt-3 mb-2">
		{#each tags as tag (tag)}
			<span class="bg-gray-100 text-xs text-blueGray-800 px-2 py-0.5 mr-1 mb-1 rounded md:text-sm">
				{tag}
			</span>
		{/each}
	</div>
	<p class="text-blueGray-600">
		{description}
	</p>
</div>
