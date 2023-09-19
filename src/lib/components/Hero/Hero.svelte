<script lang="ts">
	import { onMount } from 'svelte';
	import { fade, fly } from 'svelte/transition';
	let animate = false;

	onMount(() => {
		animate = true;
	});
</script>

{#if animate}
	<section class="layout">
		<h1 in:fly={{ y: 100, duration: 600 }}>landozone</h1>
		<h2 in:fly={{ delay: 300, y: 100, duration: 600 }}>imaginative web development</h2>

		<h3 in:fade={{ delay: 500, duration: 600 }}>
			hi! my name is <span>bruno sj</span> and I am a web developper and artist based in Berlin. I
			produce music and deejay under the alias
			<a href="https://www.instagram.com/lando.rozay" target="_blank" rel="noreferrer"
				>Orlando Rosé</a
			>. I enjoy working on creative projects where I can bring my expertise to work towards
			meaningful and innovative websites and applications.
		</h3>
	</section>
{/if}

<style>
	h1 {
		font-weight: 700;
		color: #eb6027;
		line-height: 1;
	}

	h3 {
		padding-top: 3rem /* 48px */;
		font-weight: 300;
		line-height: 1.25;
	}
</style>
