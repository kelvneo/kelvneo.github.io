<script lang="ts">
    import Fa from 'svelte-fa/src/fa.svelte'
    import { faEnvelope } from '@fortawesome/free-solid-svg-icons';
    import { faGithub, faLinkedin } from '@fortawesome/free-brands-svg-icons';
</script>

<div class="flex flex-col justify-center gap-4 px-8 py-24 md:px-32">
    <h1 class="text-purple-700 text-5xl font-bold md:text-6xl">Contact Me</h1>
    <p class="md:text-xl">
        Reach me at the following platforms:
    </p>
    <div class="flex gap-4 items-center">
        <a href="https://github.com/kelvneo" target="_blank"><Fa icon={faGithub} size="3x"></Fa></a>
        <a href="https://www.linkedin.com/in/kelvneo/" target="_blank"><Fa icon={faLinkedin} size="3x"></Fa></a>
        <a href="mailto:nkhkelvin98@gmail.com" target="_blank"><Fa icon={faEnvelope} size="3x"></Fa></a>
    </div>
</div>

