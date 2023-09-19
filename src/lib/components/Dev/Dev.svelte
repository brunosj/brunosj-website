<script lang="ts">
	import Heading from '$components/Nav/Heading.svelte';
	import LinkedIn from '$lib/assets/svg/linkedIn.svelte';
	import Social from '$components/Socials/Social.svelte';
	import Github from '$lib/assets/svg/github.svelte';
	import Website from '$lib/assets/svg/website.svelte';
	import { onMount } from 'svelte';
	import { fade, fly } from 'svelte/transition';
	let animate = false;

	onMount(() => {
		animate = true;
	});
</script>

{#if animate}
	<section class="layout" in:fly={{ y: 100, duration: 600 }}>
		<Heading title="web development" />
		<p>
			I'm a developer who enjoys bringing ideas to life on the web. In terms of technologies, my
			tools of choice are <a href="https://www.typescriptlang.org/" target="_blank" rel="noreferrer"
				>JavaScript/TypeScript</a>
			and frameworks such as
			<a href="https://kit.svelte.dev/" target="_blank" rel="noreferrer">SvelteKit</a>
			and
			<a href="https://nextjs.org/" target="_blank" rel="noreferrer">Next.js</a>. I'm particularly
			interested in dynamic and interactive data visualization, which builds on my
			<a href="https://github.com/brunosj/dna-copyright/" target="_blank" rel="noreferrer"
				>previous experience</a> with statistical software.
		</p>
		<p class="paragraph">
			My portfolio can be consulted at <a
				href="https://landozone.net"
				target="_blank"
				rel="noreferrer">landozone.net</a>
		</p>
		<div class="socials" in:fade={{ delay: 300, duration: 600 }}>
			<Social name="Portfolio" url="https://landozone.net">
				<Website />
			</Social>
			<Social name="Github" url="https://github.com/brunosj">
				<Github />
			</Social>
			<Social name="LinkedIn" url="https://www.linkedin.com/in/brunosj/">
				<LinkedIn />
			</Social>
		</div>
	</section>
{/if}

<style>
	a {
		font-family: IBMPlexMono;
		background-color: #394053;
		transition: all 300ms;
	}

	a:hover {
		background-color: #586380;
	}

	.paragraph {
		padding-top: 0.75rem;
	}
</style>
