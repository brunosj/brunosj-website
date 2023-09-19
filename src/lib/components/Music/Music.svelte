<script lang="ts">
	import Heading from '$components/Nav/Heading.svelte';
	import Social from '$components/Socials/Social.svelte';
	``;
	import Instagram from '$lib/assets/svg/instagram.svelte';
	import Projects from '$components/Projects/Projects.svelte';
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
		<Heading title="music" />
		<p>
			I am a DJ, producer and keys player. Strongly rooted in jazz and dance music, my sets and
			productions reflect the diversity of my musical influences. I am releasing music under the
			alias <a
				href="https://pinewaxrecords.com/artists/orlando-rose"
				target="_blank"
				rel="noreferrer">Orlando Rosé</a>
			and as the producer duo
			<a href="https://pinewaxrecords.com/artists/dibou" target="_blank" rel="noreferrer">dibou</a> (alongside
			uyulala).
		</p>
		<p class="paragraph">
			I am a co-founder of the <a href="https://www.shush.dance/" target="_blank" rel="noreferrer"
				>SHUSH</a>
			collective and the
			<a href="https://www.pinewaxrecords.com/" target="_blank" rel="noreferrer">Pinewax</a>
			label family. I also regularly contribute to
			<a href="https://www.thfradio.de/" target="_blank" rel="noreferrer">THF Radio</a>, where I
			host a monthly programme showcasing talents of the local scene.
		</p>

		<p class="paragraph">
			Beyond the audio realm, I have also worked on original soundtracks for various short films.
		</p>

		<div class="socials" in:fade={{ delay: 300, duration: 600 }}>
			<Social name="Instagram" url="https://instagram.com/lando.rozay">
				<Instagram />
			</Social>
			<Social name="SHUSH" url="https://shush.dance">
				<Website />
			</Social>
			<Social name="Pinewax" url="https://pinewaxrecords.com">
				<Website />
			</Social>
			<Social name="THF Radio" url="https://www.thfradio.de/shows/pinewax-radio">
				<Website />
			</Social>
		</div>

		<Projects />
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
