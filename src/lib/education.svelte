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
			subtitle: 'National University of Singapore',
			title: 'Bachelor of Computing in Information Security (with Honours)',
			caption: 'August 2020 to May 2023 (expected)',
			description: [
				'Teaching Assistant for CS2113T Software Engineering & Object-Oriented Programming for AY 21/22 Sem 2',
                'NUS Greyhats Member (2020)'
			]
		},
		{
			subtitle: 'Singapore Polytechnic',
			title: 'Diploma in Infocomm Security Management',
			caption: 'April 2015 to March 2018',
			description: [
				'Awarded Diploma with Merit (ISACA Award Recipient)',
				'President of DISM Gryphons (2016 to 2017)'
			]
		}
	];
</script>

<div class="flex flex-col justify-center gap-8 px-8 pt-32 md:px-32">
	<h1 class="text-purple-700 text-5xl font-bold md:text-6xl">Education</h1>
	<div class="flex flex-col justify-center gap-16">
		{#each data as exp}
			<Experience {...exp} />
		{/each}
	</div>
</div>
