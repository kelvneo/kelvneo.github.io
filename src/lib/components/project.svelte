<script lang="ts">
import Title from "./title.svelte";
export let title: string;
export let subtitle: string = '';
export let caption: string  = '';
export let github: string  = '';
export let description: string;
export let gallery: string[] = [];

let isOpen: boolean = false;
let currentPicture: number = 0;

function openModal(i: number) {
    isOpen = true;
    currentPicture = i;
}

</script>

<div class="flex flex-col gap-2">
    <Title {title} {subtitle} {caption} {github}></Title>
    {#if gallery.length}
    <div class="overflow-x-auto flex gap-4 border border-gray-500 p-2 rounded">
        {#each gallery as pic, i}
        <img src={pic} alt={title} class="h-48 block" on:click={() => openModal(i)}>
        {/each}
    </div>
    {/if}
    <p>{description}</p>
</div>

{#if gallery.length && isOpen}
<div class="isolate overscroll-contain z-50 bg-black/75 w-full h-full flex flex-col justify-center items-center min-h-screen gap-4 p-8 md:px-32 fixed top-0 left-0" on:click={() => isOpen = false}>
    <div class="max-w-full max-h-full border border-black dark:border-white rounded">
        <img src={gallery[currentPicture]} alt={title} class="max-w-full block max-h-full">
    </div>
</div>
{/if}
