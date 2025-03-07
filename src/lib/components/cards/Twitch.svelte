<script lang="ts">
	import type { Frame } from '$lib/components/card';
	import Card from '$lib/components/Card.svelte';

	let { id } = $props();

	let chat: Frame = {
		width: 320,
		height: 600,
		source: `https://www.twitch.tv/embed/{0}/chat?parent=${window.location.hostname}`,
		title: 'Twitch Stream'
	};

	let live: Frame = {
		width: 320,
		height: 200,
		source: `https://player.twitch.tv/?channel={0}&parent=${window.location.hostname}`,
		title: 'Twitch Chat'
	};

	const frames: Frame[] = [live, chat];
</script>

<Card
	content_id="ysnt_"
	extraStyle="border-purple-500 bg-purple-900/20 shadow-lg shadow-purple-500"
	{frames}
	input={false}
/>
