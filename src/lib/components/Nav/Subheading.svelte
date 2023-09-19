<script lang="ts">
	export let title: string;
</script>

<h3>
	{title}
</h3>

<style>
	h3 {
		padding-top: 1rem;
		margin-bottom: 1.5rem;
		font-weight: 700;
		line-height: 1;
		margin-top: -0.25rem;
	}

	@media (min-width: 1024px) {
		h3 {
			padding-top: 0px;
			margin-bottom: 2.5rem;
		}
	}
</style>
