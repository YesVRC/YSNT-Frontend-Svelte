<script lang="ts">
	let { extraStyle, frames, content_id, input = true, input_styles = "" } = $props();
	let id = $state(content_id);
</script>

<div class="m-4 flex w-fit flex-col gap-2 rounded-lg border-1 p-3 pb-auto {extraStyle}">
	{#if input}
		<input type="text" bind:value={id} class={input_styles === ""? "text-center text-white bg-blend-multiply bg-blue-400/20 backdrop-blur-lg rounded-lg px-2 border-1 border-blue-600 " : input_styles } />
	{:else}
		<p class="bg-blend-multiply bg-blue-400/20 backdrop-blur-lg rounded-lg px-2 border-1 border-blue-600 text-center text-white">{content_id}</p>
	{/if}

	{#each frames as frame (frame)}
		<iframe
			class="rounded-lg"
			src={frame.source.replace('{0}', id)}
			height={frame.height}
			width={frame.width}
			title={frame.title}
			allowfullscreen
			allow="autoplay"
		></iframe>
	{/each}
</div>
