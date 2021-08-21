<script lang="ts">
	import Project from '$lib/Project.svelte';
</script>

<svelte:head>
	<title>Projects | Ivan Wang</title>
</svelte:head>

<div class="flex flex-col max-w-3xl p-4">
	<Project
		title="Roadmap"
		link="https://roadmap.vercel.app"
		tags={['React', 'Next.js', 'Go', 'GraphQL', 'PostgreSQL']}
		description="Large scale application that uses clean architecture on the backend. Utilizes server side rendering."
	/>
	<Project
		title="Roadmap"
		link="https://roadmap.vercel.app"
		tags={['React', 'Next.js', 'Go', 'GraphQL', 'PostgreSQL']}
		description="Large scale application that uses clean architecture on the backend. Utilizes server side rendering."
	/>
</div>
<!-- Roadmap -->
<!-- https://roadmap.vercel.app -->
<!-- ['React', 'Next.js', 'Go', 'GraphQL', 'PostgreSQL'] -->
<!-- Large scale application that uses clean architecture on the backend. Utilizes server side
		rendering. -->
