<script lang="ts">
	import Dev from '$components/Dev/Dev.svelte';
	import Contact from '$components/Contact/Contact.svelte';

	import Music from '$components/Music/Music.svelte';
	import { onMount } from 'svelte';
	import { fade, fly } from 'svelte/transition';
	import Logo from '$lib/assets/svg/logo.svelte';
	import Seo from '$components/SEO/SEO.svelte';
	let animate = false;

	onMount(() => {
		animate = true;
	});
</script>

<Seo title="bruno sj" />

{#if animate}
	<section class="layout">
		<div class="logoWrapper">
			<Logo />
		</div>
		<h1 in:fly={{ y: 100, duration: 600 }}>bruno sj</h1>
		<h2 in:fly={{ delay: 300, y: 100, duration: 600 }}>web developper & artist</h2>

		<p in:fade={{ delay: 500, duration: 600 }}>
			hi! my name is <span>bruno sj</span> and I am a web developper and artist based in Berlin.
		</p>
	</section>
{/if}

{#if animate}
	<div class="mobileSection" in:fade={{ delay: 500, duration: 600 }}>
		<Dev />
	</div>

	<div class="mobileSection" in:fade={{ delay: 500, duration: 600 }}>
		<Music />
	</div>

	<div class="mobileSection" in:fade={{ delay: 500, duration: 600 }}>
		<Contact />
	</div>
{/if}

<style>
	h1 {
		font-weight: 700;
		color: #eb6027;
		line-height: 1;
	}

	p {
		padding-top: 3rem /* 48px */;
	}

	a {
		font-family: IBMPlexMono;
		background-color: #394053;
		transition: all 300ms;
	}

	a:hover {
		background-color: #586380;
	}

	.name {
		font-weight: 700;
	}

	.mobileSection {
		display: block;
	}

	.logoWrapper {
		display: block;
		height: 2rem;
		width: 2rem;
		margin-bottom: 0.75rem;
	}

	@media (min-width: 768px) {
		.logoWrapper {
			display: none;
		}
	}
	@media (min-width: 1024px) {
		.mobileSection {
			display: none;
		}
	}
</style>
