<script lang="ts">
	import Link from '$lib/assets/link.svg?component';
</script>

<div class="col-start-1 col-end-13 px-4 sm:col-start-2 sm:col-end-12 sm:px-0">
	<section class="grid grid-cols-2 gap-y-2 gap-x-6 mb-8">
		<div class="col-span-2 w-full md:col-span-1">
			<div class="ratio bg-blue-100" />
		</div>
		<div class="col-span-2 md:col-span-1">
			<h3 class="text-2xl font-bold">
				<a href="https://roadmap.vercel.app" rel="noopener noreferrer" target="_blank">Roadmap</a>
			</h3>
			<a href="/" class="flex items-center text-gray-400">
				<Link class="w-4 h-4 fill-current mr-2" />
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
	</section>
</div>
