<script lang="ts">
	import '../app.css';
	import NavBar from '$lib/components/NavBar.svelte';
	let { children } = $props();
</script>

<head>
	<meta charset="utf-8"/>
	<meta property="og:title" content="Y S N T" />
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://ysnt.live" />
	<meta property="og:image" content="https://images-ext-1.discordapp.net/external/2WnlpFrzfqe6j9fLIfoO6juHHK_0knPujHLxvCeA600/%3Fsize%3D64x64/https/cdn.discordapp.com/avatars/886794795866030100/cdb4ca9ac8e4892857712b728039614b.png?&quality=lossless&width=128&height=128" />
	<meta property="og:description" content="Yes's Website idk man" />
	<meta name="theme-color" content="#9900FF">

	<!-- Include this to make the og:image larger -->
	<meta name="twitter:card" content="summary_large_image">
</head>

<NavBar/>
{@render children()}
