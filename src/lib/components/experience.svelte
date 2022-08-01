<script lang="ts">
	import Title from './title.svelte';
	export let title: string;
	export let subtitle = '';
	export let caption = '';
	export let github = '';
	export let description: string[] = [];
</script>

<div class="flex flex-col gap-2">
	<Title {title} {subtitle} {caption} {github} />
	{#if description.length}
		<ul class="list-inside list-disc">
			{#each description as li}
				<li>{li}</li>
			{/each}
		</ul>
	{/if}
</div>
