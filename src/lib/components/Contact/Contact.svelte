<script lang="ts">
	import Heading from '$components/Nav/Heading.svelte';
	import { onMount } from 'svelte';
	import { fade, fly } from 'svelte/transition';
	import LinkedIn from '$lib/assets/svg/linkedIn.svelte';
	import Social from '$components/Socials/Social.svelte';
	import Github from '$lib/assets/svg/github.svelte';
	import Instagram from '$lib/assets/svg/instagram.svelte';

	let animate = false;

	onMount(() => {
		animate = true;
	});
</script>

{#if animate}
	<section class="layout" in:fly={{ y: 100, duration: 600 }}>
		<Heading title="contact" />
		<p>Curious about collaborating on projects?</p>
		<p class="paragraph">Get in touch at:</p>
		<p>
			<span class="contactMail">
				<span>mail </span>
				<span class="contactMailGreen ">[at]</span>
				<span>brunosj</span>
				<span class="contactMailGreen ">[dot]</span>
				<span>com</span>
			</span>
		</p>
		<div class="socials" in:fade={{ delay: 300, duration: 600 }}>
			<Social name="LinkedIn" url="https://www.linkedin.com/in/brunosj/">
				<LinkedIn />
			</Social>
			<Social name="Instagram" url="https://instagram.com/lando.rozay">
				<Instagram />
			</Social>
		</div>
	</section>
{/if}

<style>
	.paragraph {
		padding-top: 0.75rem;
	}

	.contactMail {
		letter-spacing: -0.05rem;
		font-weight: 700;
	}

	.contactMailGreen {
		color: #eb6027;
	}
</style>
