<script lang="ts">
	
	import Fa from 'svelte-fa/src/fa.svelte';
	import { faMoon, faSun } from '@fortawesome/free-solid-svg-icons';
	import { onMount } from 'svelte';
	let menuOpened = false;
	let dark = true;

	function toggleTheme() {
		dark = !dark
		saveTheme()
	}

	function saveTheme() {
		if (localStorage) {
			if (dark) {
				localStorage.setItem('dark', 'true');
			} else {
				localStorage.setItem('dark', 'false');
			}
		}
		if (dark) {
			document.documentElement.classList.add('dark');
		} else {
			document.documentElement.classList.remove('dark');
		}
	}

	onMount(() => {
		if (localStorage.dark === 'true' || (!('dark' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
			dark = true;
		} else {
			dark = false;
		}
		saveTheme();
	});

</script>

<nav class="lg:bg-white lg:dark:bg-neutral-900 fixed p-4 min-w-full flex flex-col border-gray-200 dark:border-gray-800 lg:border-b-0" class:border-b={menuOpened} class:bg-white={menuOpened} class:dark:bg-neutral-900={menuOpened}>
	<div class="flex justify-end">
		<button
			on:click={() => (menuOpened = !menuOpened)}
			on:keypress={() => (menuOpened = !menuOpened)}
			data-collapse-toggle="navbar-default"
			type="button"
			class="inline-flex items-center p-2 ml-3 text-sm text-gray-500 rounded-lg bg-gray-100/75 dark:bg-neutral-800/75 lg:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
			aria-controls="navbar-default"
			aria-expanded="false"
		>
			<span class="sr-only">Open main menu</span>
			<svg
				class="w-6 h-6"
				aria-hidden="true"
				fill="currentColor"
				viewBox="0 0 20 20"
				xmlns="http://www.w3.org/2000/svg"
				><path
					fill-rule="evenodd"
					d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
					clip-rule="evenodd"
				/></svg
			>
		</button>
	</div>
	<div class:hidden={!menuOpened} class="grow w-full lg:block lg:w-auto" id="navbar-default">
		<ul
			on:click={() => (menuOpened = false)}
			on:keypress={() => (menuOpened = false)}
			class="flex flex-col text-right p-4 mt-4 gap-4 lg:gap-0 lg:flex-row lg:space-x-8 lg:mt-0 lg:text-sm lg:font-medium lg:border-0 lg:justify-end"
		>
			<li><a href="#about-me">About Me</a></li>
			<li><a href="#experiences">Experiences</a></li>
			<li><a href="#projects">Projects</a></li>
			<li><a href="#education">Education</a></li>
			<li><a href="#contact-me">Contact Me</a></li>
			<li>
				<button on:click|stopPropagation={toggleTheme} class="align-middle"
					>
					{#if dark}
					<span class="lg:hidden mr-2">Light Mode</span><Fa icon={faSun} class="inline-block"/>
					{:else}
					<span class="lg:hidden mr-2">Dark Mode</span><Fa icon={faMoon} class="inline-block"/>
					{/if}
				</button>
			</li>
		</ul>
	</div>
</nav>
