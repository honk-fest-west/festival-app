<script lang="ts">
	import FestivalApp from '$lib/FestivalApp.svelte';
	import type { ConfigParams } from '$types';
	import type { PageData } from './$types.js';

	let { data }: { data: PageData } = $props();

	let config: ConfigParams = {
		days: data.days,
		artists: data.artists,
		stages: data.stages,
		options: data.options
	};
</script>

<div class="fullscreen-preview">
	<FestivalApp {config} />
</div>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
	}
	.fullscreen-preview {
		position: fixed;
		top: 0;
		left: 0;
		width: 100lvw;
		height: 100lvh;
	}
</style>
