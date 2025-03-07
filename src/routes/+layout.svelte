<script lang="ts">
	import '../app.css';
	import NavBar from '$lib/components/NavBar.svelte';
	let { children } = $props();
</script>

<svelte:head>
	<title>YSNT</title>
	<meta charset="utf-8"/>
	<meta property="og:title" content="Y S N T" />
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://ysnt.live" />
	<meta property="og:image" content="https://ysnt.live/embed.png" />
	<meta property="og:description" content="Yes's Website idk man" />
	<meta name="theme-color" content="#000000">

	<!-- Include this to make the og:image larger -->
	<meta name="twitter:card" content="summary_large_image">
</svelte:head>

<NavBar/>
{@render children()}
