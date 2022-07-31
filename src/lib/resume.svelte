<script lang="ts">
    import Fa from 'svelte-fa/src/fa.svelte'
    import { faDownload } from '@fortawesome/free-solid-svg-icons';
</script>

<div class="flex flex-col justify-center min-h-screen gap-4 px-8 py-24 md:px-32">
    <h1 class="text-purple-700 text-7xl font-bold">Resume</h1>
    <p class="md:text-xl">
        You can download my resume with the button below (Updated 20 July 2022).
    </p>
    <div class="mt-2">
        <a href="./Neo Ken Hong Kelvin Resume.pdf" target="_blank" class="border px-3 py-2 rounded inline-flex items-center gap-2">
            <Fa icon={faDownload} pull="left"></Fa> Download
        </a>
    </div>
</div>

