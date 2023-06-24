<script lang="ts">
	import Fa from 'svelte-fa/src/fa.svelte';
	import { faGithub } from '@fortawesome/free-brands-svg-icons';
</script>

<div class="flex flex-col justify-center gap-4 pt-24">
	<h1 class="text-cyan-700 text-5xl font-bold md:text-6xl">About Me</h1>
	<p class="md:text-xl">
		I am interested in anything technology-related, especially in cybersecurity. As more people and
		organizations connect and digitalize their lives, I love to understand how technology works and how to
		secure them. I am also interested in software engineering and web development, and I have built a few web
		applications as part of my school and work projects.
	</p>
	<p class="md:text-xl">
		I occasionally play Capture The Flag (CTF) competitions with my friends under 
		<a href="https://github.com/Dame-Dango" target="_blank" rel="noreferrer" class="inline">
			<Fa icon={faGithub} size="lg" class="inline"/>
			<span>Dame Dango.</span>
		</a> You can view the writeups of the CTFs that I have participated in with my team in the team repository.
	</p>
	<p class="md:text-xl">
		I am currently working as a Backend Engineer at TikTok Singapore.
	</p>
</div>
