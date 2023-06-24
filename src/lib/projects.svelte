<script lang="ts">
	import Project from './components/project.svelte';

	interface Proj {
		title: string;
		subtitle: string;
		caption: string;
		github?: string;
		description: string;
		gallery?: string[];
	}

	const data: Proj[] = [
		{
			title: 'TraceIT - Pandemic Tracing System',
			github: 'https://github.com/IFS4205-TraceIT/',
			caption: 'August 2022 to November 2022',
			subtitle: 'Nuxt 3, Django Rest Framework, HashiCorp Vault, PostgreSQL, and Ansible',
			description: 'TraceIT aims to be a prototype national pandemic tracing system that utilises information technology to monitor the outbreak and spread of a disease.'
		},
		{
			title: 'My Portfolio',
			github: 'https://github.com/kelvneo/kelvneo.github.io',
			caption: 'August 2022',
			subtitle: 'Svelte, Tailwind and FontAwesome',
			description: 'The website you are viewing now!'
		},
		{
			title: 'Eleos - Decentralized Charity Platform',
			github: 'https://github.com/IS4302-Eleos/Eleos',
			caption: 'January 2022 to April 2022',
			subtitle: 'Nuxt.js, Koa, Ganache, Truffle and MongoDB',
			description:
				'Eleos is built as a decentralized Web 3.0 application (dApps) to remove the middleman of charity fundraisers.',
			gallery: ['eleos-1.png', 'eleos-2.png', 'eleos-3.png']
		},
		{
			title: 'TermiNUS',
			github: 'https://github.com/AY2122S1-CS2113T-T10-2/tp',
			caption: 'August 2021 to November 2021',
			subtitle: 'Java',
			description:
				'TermiNUS is a CLI (command line interface) program for NUS Students who wish to organize their NUS academic materials through a CLI. It supports features such as notes, schedule management, and active recall.'
		},
		{
			title: 'The Off App',
			github: 'https://github.com/kelvneo/TheOffApp',
			caption: 'January 2021 to August 2021',
			subtitle: 'Vue.js, Buefy and Firebase',
			description:
				'The Off App (TOA) is built to replace the manual process of applying for Off Passes for NSFs.',
			gallery: ['toa-0.png', 'toa-1.png', 'toa-2.png', 'toa-3.png', 'toa-4.jpg']
		},
		{
			title: 'ArcaDOVE',
			caption: 'September 2017 to February 2018',
			subtitle: 'Angular, Express, Docker and MySQL',
			description:
				'ArcaDOVE is an automated web environment platform that aims to provide a quick and easy way for web developers to deploy and test their web applications without having to worry about the hassle of incompatibilities.'
		}
	];
</script>

<div class="flex flex-col justify-center gap-8 pt-32">
	<h1 class="text-cyan-700 text-5xl font-bold md:text-6xl">Projects</h1>
	<div class="flex flex-col justify-center gap-16">
		{#each data as proj}
			<Project {...proj} />
		{/each}
	</div>
</div>
