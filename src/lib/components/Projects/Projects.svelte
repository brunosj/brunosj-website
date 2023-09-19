<script lang="ts">
	import { releases } from '$lib/data/releases';
	import { films } from '$lib/data/film';
	import Heading from '$components/Nav/Heading.svelte';
	import Subheading from '$components/Nav/Subheading.svelte';

	// Sort releases by year (newest to oldest)
	releases.sort((a, b) => b.year - a.year);

	// Sort films by year (newest to oldest)
	films.sort((a, b) => b.year - a.year);
</script>

<section class="">
	<Subheading title="releases" />
	<ul class="releases">
		{#each releases as release}
			<a href={release.stream} target="_blank" rel="noreferrer" class="releaseWrapper">
				<li class="release">
					<h4>
						{release.artist}
					</h4>
					<p>
						{release.title}
					</p>
					<p>-</p>
					<p>
						{release.year}
					</p>
				</li>
			</a>
		{/each}
	</ul>
</section>
<section>
	<Subheading title="film soundtracks" />
	<ul class="soundtracks">
		{#each films as film}
			<li class="soundtrack">
				<h4>
					{film.name}
				</h4>
				<p>
					{film.year}
				</p>
				<p>
					Directed by: {film.director}
				</p>
			</li>
		{/each}
	</ul>
</section>

<style>
	.releases {
		display: flex;
		gap: 2rem;
		flex-wrap: wrap;
	}

	.releaseWrapper {
		width: 100%;
		border-width: 1px;
		transition: background-color 300ms ease-in-out;
		border-radius: 0.375rem;
		border-color: #eb6027;
	}

	.release {
		width: 100%;
		display: flex;
		align-items: center;
		/* justify-content: space-around; */
		/* gap: 0.75rem; */
		padding: 0.75rem;
	}

	.releaseWrapper:hover {
		background-color: #586380;
	}

	.soundtracks {
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}

	.soundtrack {
		width: 100%;
	}

	.soundtrack h4 {
		color: #eb6027;
		font-weight: 700;
	}

	section {
		padding-top: 3rem;
	}

	.release p {
		padding-left: 2rem;
		font-size: medium;
	}

	.release h4 {
		color: #eb6027;
		font-weight: 700;
	}

	.soundtrack p {
		font-size: medium;
	}

	a {
		transition: all 300ms ease-in-out;
	}

	a:hover {
		background-color: #9795f0;
	}

	.link {
		display: inline;
		font-size: 1rem;
		line-height: 1.5rem;
	}

	@media (max-width: 768px) {
		p {
			font-size: 1.125rem /* 18px */;
			line-height: 1.75rem /* 28px */;
		}

		.release p {
			padding-left: 0rem;
		}

		.release {
			flex-direction: column;
			display: flex;
			align-items: start;
		}

		section {
			padding-top: 1.5rem;
		}
	}
</style>
