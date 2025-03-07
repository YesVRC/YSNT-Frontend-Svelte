<script lang="ts">
	import type { Frame } from '$lib/components/card';
	import Card from '$lib/components/Card.svelte';

	let { id } = $props();
	const frames: Frame[] = [
		{
			width: 320,
			height: 200,
			title: 'Youtube Stream',
			source: `https://youtube.com/embed/{0}?&autoplay=1&mute=1`
		},
		{
			width: 320,
			height: 600,
			title: 'Youtube Chat',
			source: `https://www.youtube.com/live_chat?v={0}&embed_domain=${window.location.hostname}`
		}
	]
</script>

<Card
	content_id={id}
	extraStyle="border-red-500 bg-red-900/20 shadow-lg shadow-red-500"
	frames={frames}
/>
