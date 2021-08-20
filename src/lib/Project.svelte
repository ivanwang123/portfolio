<script lang="ts">
	import Link from '$lib/assets/link.svg?component';
</script>

<div class="col-span-2 w-full md:col-span-1">
	<div class="border rounded-md overflow-hidden">
		<div class="flex items-center h-7 bg-gray-100 px-4">
			<div class="w-3 h-3 bg-red-400 mr-2 rounded-full" />
			<div class="w-3 h-3 bg-yellow-400 mr-2 rounded-full" />
			<div class="w-3 h-3 bg-green-400 mr-2 rounded-full" />
		</div>
		<img src="res/screenshot1.png" alt="screenshot" />
	</div>
</div>
<div class="col-span-2 mb-10 md:col-span-1 md:mb-0">
	<h3 class="text-xl font-bold">
		<a href="https://roadmap.vercel.app" rel="noopener noreferrer" target="_blank">Roadmap</a>
	</h3>
	<a
		class="flex items-center w-max text-gray-400"
		href="https://roadmap.vercel.app"
		rel="noopener noreferrer"
		target="_blank"
	>
		<Link class="w-4 h-4 fill-current mr-1" />
		roadmap.vercel.app
	</a>
	<div class="flex flex-wrap mt-3 mb-2">
		{#each ['React', 'Next.js', 'Go', 'GraphQL', 'PostgreSQL'] as tag (tag)}
			<span class="bg-gray-100 text-xs px-2 py-0.5 mr-1 mb-1 rounded md:text-sm">{tag}</span>
		{/each}
	</div>
	<p>
		Large scale application that uses clean architecture on the backend. Utilizes server side
		rendering.
	</p>
</div>
