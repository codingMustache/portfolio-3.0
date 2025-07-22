<script>
	import Logo from '$lib/components/logo.svelte';
	import CallToAction from '$lib/components/call-to-action.svelte';
	import Bio from '$lib/components/bio.svelte';
	import Projects from '$lib/components/projects.svelte';
</script>

<main>
	<section>
		<Logo />
	</section>
	<section>
		<CallToAction />
	</section>
	<section>
		<Bio />
	</section>
	<section>
		<Projects />
	</section>
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		justify-content: center;
	}
	section {
		width: 100%;
	}
</style>
