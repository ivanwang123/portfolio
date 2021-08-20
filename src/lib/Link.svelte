<script lang="ts">
	export let path: string;
	export let label: string;
</script>

<a class="hvr-shutter-out-vertical text-blue-500 px-4" sveltekit:prefetch href={path}>{label}</a>
