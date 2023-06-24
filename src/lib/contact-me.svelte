<script lang="ts">
	import Fa from 'svelte-fa/src/fa.svelte';
	import { faEnvelope, faDownload } from '@fortawesome/free-solid-svg-icons';
	import { faGithub, faLinkedin } from '@fortawesome/free-brands-svg-icons';
</script>

<div class="flex flex-col justify-center gap-8 py-24">
	<h1 class="text-cyan-700 text-5xl font-bold md:text-6xl">Contact Me</h1>
	<div class="flex flex-col justify-center mb-2 gap-2">
		<h4 class="text-3xl font-bold">
			Social Media
		</h4>
		<p class="md:text-xl">Reach me at the following platforms:</p>
		<div class="flex gap-4 items-center mt-2">
			<a href="https://github.com/kelvneo" target="_blank" rel="noreferrer"><Fa icon={faGithub} size="3x" /></a>
			<a href="https://www.linkedin.com/in/kelvneo/" target="_blank" rel="noreferrer">
				<Fa icon={faLinkedin} size="3x" />
			</a>
			<a href="mailto:nkhkelvin98@gmail.com" target="_blank"><Fa icon={faEnvelope} size="3x" /></a>
		</div>
	</div>
	
	<div class="flex flex-col justify-center gap-2">
		<h4 class="text-3xl font-bold">
			Resume Download
		</h4>
		<p class="md:text-xl">You can download my resume with the button below:</p>
		<div class="mt-2 flex flex-col gap-2 items-start md:items-center md:flex-row">
			<a
				href="./KelvinNeo_Resume.pdf"
				target="_blank"
				class="border px-3 py-2 rounded inline-flex items-center gap-2"
			>
				<Fa icon={faDownload} pull="left" /> Download
			</a>
			<span class="text-gray-500">Last Updated: 24 June 2023</span>
		</div>
	</div>
</div>
