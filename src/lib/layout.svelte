<script>
	import AboutMe from './about-me.svelte';
	import ContactMe from './contact-me.svelte';
    import Education from './education.svelte';
	import Experiences from './experiences.svelte';
	import Hi from './hi.svelte';
	import Projects from './projects.svelte';
</script>

<svelte:head>
	<title>Kelvin Neo</title>
	<meta name="description" content="Hello! I am Kelvin Neo, and this is a techie's personal portfolio webpage, showcasing my latest projects and experiences. "/>
</svelte:head>

<div>
	<div class="">
		<section id="Hi"><Hi /></section>
		<section id="about-me"><AboutMe /></section>
		<section id="experiences"><Experiences /></section>
		<section id="projects"><Projects /></section>
		<section id="education"><Education /></section>
		<section id="contact-me"><ContactMe /></section>
	</div>
</div>

<style>
	/* .content {
    scroll-snap-points-y: repeat(300px);
    scroll-snap-type: y mandatory;
    scroll-snap-type: mandatory;
    overflow: auto;
}

.content section {
    scroll-snap-align: start;
} */
</style>
