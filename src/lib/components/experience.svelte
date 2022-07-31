<script lang="ts">
    import Title from "./title.svelte";
    export let title: string;
    export let subtitle: string = '';
    export let caption: string  = '';
    export let github: string  = '';
    export let description: string[] = [];
</script>

<div class="flex flex-col gap-2">
    <Title {title} {subtitle} {caption} {github}></Title>
    {#if description.length}
    <ul class="list-inside list-disc">
        {#each description as li}
        <li>{li}</li>
        {/each}
    </ul>
    {/if}
</div>
        