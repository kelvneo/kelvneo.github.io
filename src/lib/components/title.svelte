<script lang="ts">
	import Fa from 'svelte-fa/src/fa.svelte';
	import { faGithub } from '@fortawesome/free-brands-svg-icons';
	export let title = '';
	export let subtitle = '';
	export let caption = '';
	export let github = '';

	$: showSeparator = title && github;
	$: repoName = github.replace('https://github.com/', '@').replace(/\/$/, '');
</script>

<div class="flex flex-col gap-1">
	<div class="flex gap-2 flex-col lg:items-center lg:flex-row">
		<h4 class="text-3xl font-bold">
			{title}
		</h4>
		{#if showSeparator}
			<span class="hidden lg:block">&#8226;</span>
		{/if}
		{#if github}
			<a href={github} target="_blank" rel="noreferrer" class="flex gap-2 items-center">
				<Fa icon={faGithub} size="lg"/>
				<span class="text-gray-600 dark:text-gray-400 text-lg">{repoName}</span>
			</a>
		{/if}
	</div>
	<div class="flex gap-2 items-center">
		<h1 class="text-xl dark:text-gray-300">{subtitle}</h1>
	</div>
	<h4 class="text-md text-gray-500">{caption}</h4>
</div>
