<script lang="ts">
import Title from "./title.svelte";
export let title: string;
export let subtitle: string = '';
export let caption: string  = '';
export let github: string  = '';
export let description: string;
export let gallery: string[] = [];
</script>

<div class="flex flex-col gap-2">
    <Title {title} {subtitle} {caption} {github}></Title>
    {#if gallery.length}
    <div class="overflow-x-auto flex gap-4 border border-gray-500 p-2 rounded">
        {#each gallery as pic}
        <img src={pic} alt={title} class="h-48 block">
        {/each}
    </div>
    {/if}
    <p>{description}</p>
</div>



