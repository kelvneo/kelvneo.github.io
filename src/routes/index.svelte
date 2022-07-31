<script>
import AboutMe from "$lib/about-me.svelte";
import ContactMe from "$lib/contact-me.svelte";
import Experiences from "$lib/experiences.svelte";
import Hi from "$lib/hi.svelte";
import Projects from "$lib/projects.svelte";
import Resume from "$lib/resume.svelte";

</script>

<svelte:head>
	<title>Kelvin Neo</title>
</svelte:head>

<div>
    <div class="">
        <section id="Hi"><Hi></Hi></section>
        <section id="about-me"><AboutMe></AboutMe></section>
        <section id="experiences"><Experiences></Experiences></section>
        <section id="projects"><Projects></Projects></section>
        <section id="resume"><Resume></Resume></section>
        <section id="contact-me"><ContactMe></ContactMe></section>
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
