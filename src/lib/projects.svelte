<script lang="ts">
import Project from "./components/project.svelte";

const data: any[] = [
    {
        title: "My Portfolio",
        github: "https://github.com/kelvneo/",
        subtitle:"August 2022",
        caption: "Built with Svelte, Tailwind and FontAwesome",
        description: "The website you are viewing now!"
    }, {
        title: "Eleos - Decentralized Charity Platform",
        github: "https://github.com/IS4302-Eleos/Eleos", 
        subtitle: "January 2022 to April 2022",
        caption: "Built with Nuxt.js, Koa, Ganache, Truffle and MongoDB",
        description: "Eleos is built as a decentralized Web 3.0 application (dApps) to remove the middleman of charity fundraisers.",
        gallery: ["eleos-1.png", "eleos-2.png", "eleos-3.png"]
    }, {
        title: "TermiNUS",
        github: "https://github.com/AY2122S1-CS2113T-T10-2/tp",
        subtitle: "August 2021 to November 2021",
        caption: "Built with Java",
        description: "TermiNUS is a CLI (command line interface) program for NUS Students who wish to organize their NUS academic materials through a CLI. It supports features such as notes, schedule management, and active recall."

    }, {
        title: "The Off App",
        github: "https://github.com/kelvneo/TheOffApp",
        subtitle: "January 2021 to August 2021",
        caption: "Built with Vue.js, Buefy and Firebase",
        description: "The Off App (TOA) is built to replace the manual process of applying for Off Passes for NSFs.",
        gallery: ["toa-0.png", "toa-1.png", "toa-2.png", "toa-3.png", "toa-4.jpg"]
    }, {
        title: "ArcaDOVE",
        github:"https://github.com/kelvneo/TheOffApp",
        subtitle: "Septemer 2017 to February 2018",
        caption: "Built with Angular, Express, Docker and MySQL",
        description:"ArcaDOVE is an automated web environment platform that aims to provide a quick and easy way for web developers to deploy and test their web applications without having to worry about the hassle of incompatibilities."
    }
]
</script>

<div class="flex flex-col justify-center min-h-screen gap-8 px-8 py-32 md:px-32">
    <h1 class="text-purple-700 text-7xl font-bold">Projects</h1>
    <div class="flex flex-col justify-center gap-24">
        {#each data as proj}
            <Project {...proj}></Project>
        {/each}

    </div>
</div>

