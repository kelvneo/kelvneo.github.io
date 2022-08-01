<script lang="ts">
	import Fa from 'svelte-fa/src/fa.svelte';
	import { faGithub } from '@fortawesome/free-brands-svg-icons';
	export let title = '';
	export let subtitle = '';
	export let caption = '';
	export let github = '';

	$: showSeparator = subtitle && github;
</script>

<div class="flex flex-col gap-1">
	<h4 class="text-3xl font-bold">{title}</h4>
	<div class="flex gap-2 items-center">
		{#if github}
			<a href={github} target="_blank"><Fa icon={faGithub} size="lg" /></a>
		{/if}
		{#if showSeparator}
			<span>&#8226;</span>
		{/if}
		<h1 class="text-xl dark:text-gray-300">{subtitle}</h1>
	</div>
	<h4 class="text-md text-gray-500">{caption}</h4>
</div>
