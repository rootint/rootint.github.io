<script context="module">
	import { browser, dev } from '$app/env';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="content">
	<h1>My Projects</h1>
	<p style="color: #fff">
		<a href="https://github.com/orgs/InnoSWP/projects/9">ReusEd Learning</a>
		- a project that we are doing with my fantastic team at Innopolis.
	</p>
	<div class="spacer" />
	<h2>
		Unfortunately, I don't have many projects now.<br /> However, you can always come up to me and suggest
		something super cool, I would not be against.
	</h2>
</div>

<style>
	h2 {
		font-style: italic;
	}
	.content {
		text-align: center;
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}
	.spacer {
		margin: 50px;
	}
	.smallspacer {
		margin: 16px;
	}
</style>
