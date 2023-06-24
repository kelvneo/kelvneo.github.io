<script lang="ts">
	import Experience from './components/experience.svelte';

	interface Exp {
		title: string;
		subtitle: string;
		caption: string;
		description: string[];
	}

	const data: Exp[] = [
		{
			title: 'Backend Engineer',
			subtitle: 'TikTok / ByteDance',
			caption: 'June 2023 to Present',
			description: []
		},
		{
			title: 'Software Engineer Intern',
			subtitle: 'Visa Inc',
			caption: 'May 2022 to August 2022',
			description: [
				'Developed user interface for automation with ASP.NET and Javascript for network operations team, reducing error from manual checks in OSPF and BGP servers.'
			]
		},
		{
			title: 'Information Security Engineer - Freelancer',
			subtitle: 'PayPal',
			caption: 'December 2021 to April 2022',
			description: [
				'Developed and maintained secure data sharing platform using Private Set Intersection and Homomorphic Encryption in Go and C++, ensuring privacy and security of both parties.',
				'Collaborated with Nanyang Technological University on Multi-Party Computation, improving security and redundancy of cryptography services.'
			]
		},
		{
			title: 'Lead Programmer',
			subtitle: 'Singapore Armed Forces',
			caption: 'January 2019 to August 2020',
			description: [
				'Contributed to the COVID-19 fighting efforts by reducing administrative overhead through sending of medical appointment messages automatically through AWS and NodeJS.',
				'Reduced accounting errors in logistics by developing mobile application software to track expenditure of equipment using Dart and Flutter.',
				'Improved welfare of colleagues by transitioning paper based off-taking system to an online system with VueJS and Firebase'
			]
		},
		{
			title: 'Research and Development Intern',
			subtitle: 'Singapore Telecommunications Limited',
			caption: 'April 2017 to August 2017',
			description: [
				'Provided reliable data ingestion for large volumes of streaming data into machine learning network through Apache Kafka and Scala.',
				'Supported government project to monitor malicious traffic using statistical analysis methods using Iguazio Platform, Python and Netflow.'
			]
		}
	];
</script>

<div class="flex flex-col justify-center gap-8 pt-32">
	<h1 class="text-cyan-700 text-5xl font-bold md:text-6xl">Experiences</h1>
	<div class="flex flex-col justify-center gap-16">
		{#each data as exp}
			<Experience {...exp} />
		{/each}
	</div>
</div>
