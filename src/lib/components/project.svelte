<script lang="ts">
	import Title from './title.svelte';
	import Fa from 'svelte-fa/src/fa.svelte';
	import { faChevronLeft, faChevronRight } from '@fortawesome/free-solid-svg-icons';

	export let title: string;
	export let subtitle = '';
	export let caption = '';
	export let github = '';
	export let description: string;
	export let gallery: string[] = [];

	let isOpen = false;
	let currentPicture = 0;

	function openModal(i: number) {
		isOpen = true;
		currentPicture = i;
	}

	function previousPicture() {
		currentPicture = Math.max(0, currentPicture - 1);
	}

	function nextPicture() {
		currentPicture = Math.min(gallery.length - 1, currentPicture + 1);
	}

	function onKeyDown(e: KeyboardEvent) {
		if (!isOpen) {
			return;
		}

		switch (e.key) {
			case 'ArrowLeft':
				previousPicture();
				break;
			case 'ArrowRight':
				nextPicture();
				break;
			case 'Escape':
				isOpen = false;
				break;
		}
	}

</script>

<div class="flex flex-col gap-2">
	<Title {title} {subtitle} {caption} {github} />
	{#if gallery.length}
		<div class="overflow-x-auto flex gap-4 border border-gray-500 p-2 rounded">
			{#each gallery as pic, i}
				<img src={pic} alt={title} class="h-48 block" on:click={() => openModal(i)} on:keypress={() => openModal(i)}/>
			{/each}
		</div>
		{#if isOpen}
			<div
				class="isolate overscroll-contain z-50 bg-black/75 w-full h-full flex flex-col justify-center items-center min-h-screen gap-4 p-8 md:px-32 fixed top-0 left-0"
				on:click|once={() => (isOpen = false)}  on:keypress={() => {isOpen = false}}
			>
				<div class="max-w-full max-h-full border border-black dark:border-white rounded">
					<img src={gallery[currentPicture]} alt={title} class="max-w-full block max-h-full" />
				</div>
				<!-- <p class="text-white">Click anywhere to close</p> -->
				<div class="flex gap-8">
					<button on:click|stopPropagation={previousPicture}
						><Fa icon={faChevronLeft} size="xl" />
					</button>
					<button on:click|stopPropagation={nextPicture}
						><Fa icon={faChevronRight} size="xl" />
					</button>
				</div>
			</div>
		{/if}
	{/if}
	<p>{description}</p>
</div>

<svelte:window on:keydown={onKeyDown}/>
