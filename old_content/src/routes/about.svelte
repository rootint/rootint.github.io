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
	<title>Abou Me</title>
	<meta name="description" content="About Me" />
</svelte:head>

<div class="content">
    <h1>About Me</h1>
    <img src="me.png" width=200 alt="myface">
	<p style="color: #fff">
        I have a lot of hobbies, like solving the Rubik's Cube, playing the
        piano, writing music and sleeping:)<br /><br />
        Furthermore, I am extremely fond of Mobile Development, I know Flutter
        pretty well and currently learning SwiftUI. <br /><br />
        I also particularly enjoy playing badminton.
      </p>
</div>

<style>
	.content {
        text-align: center;
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}
</style>
