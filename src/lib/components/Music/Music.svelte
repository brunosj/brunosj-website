<script lang="ts">
	import Heading from '$components/Nav/Heading.svelte';
	import Social from '$components/Socials/Social.svelte';
	``;
	import Instagram from '$lib/assets/svg/instagram.svelte';
	import Projects from '$components/Projects/Projects.svelte';
	import Website from '$lib/assets/svg/website.svelte';
</script>

<section class="layout">
	<Heading title="music" />
	<p>
		I am a DJ, producer and keys player. Strongly rooted in jazz and dance music, my sets and
		productions reflect the diversity of my musical influences. I have released music on my own and
		with collaborators (under the moniker <a
			href="https://pinewaxrecords.com/artists/orlando-rose"
			target="_blank"
			rel="noreferrer">Orlando Rosé</a>
		), as well as the producer duo
		<a href="https://pinewaxrecords.com/artists/dibou" target="_blank" rel="noreferrer">dibou</a> (together
		with uyulala).
	</p>
	<p class="paragraph">
		I am a co-founder of the <a href="https://www.shush.dance/" target="_blank" rel="noreferrer"
			>SHUSH</a>
		collective and the
		<a href="https://www.pinewaxrecords.com/" target="_blank" rel="noreferrer">Pinewax</a>
		label family. I also regularly contribute to
		<a href="https://www.thfradio.de/shows/pinewax-radio" target="_blank" rel="noreferrer"
			>THF Radio</a
		>, where I host a monthly programme showcasing talents of the local scene.
	</p>

	<p class="paragraph">
		Beyond the audio realm, I have also worked on original soundtracks for various short films.
	</p>

	<div class="socials">
		<Social name="Instagram" url="https://instagram.com/lando.rozay">
			<Instagram />
		</Social>
		<Social name="SHUSH" url="https://shush.dance">
			<Website />
		</Social>
		<Social name="Pinewax" url="https://pinewaxrecords.com">
			<Website />
		</Social>
	</div>

	<Projects />
</section>

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

	.socials {
		margin-top: 2.5rem;
		display: flex;
		gap: 3rem;
	}

	@media (max-width: 768px) {
		.socials {
			display: inline-flex;
			flex-direction: column;
			gap: 1rem;
		}
	}
</style>
