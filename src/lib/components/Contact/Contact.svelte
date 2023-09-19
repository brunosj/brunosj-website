<script lang="ts">
	import Heading from '$components/Nav/Heading.svelte';
</script>

<section>
	<div class="layout">
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
	</div>
</section>

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
