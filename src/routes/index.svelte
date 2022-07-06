<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import Joke from '$lib/Joke.svelte';
</script>

<svelte:head>
	<title>Danil Timofeev</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<Joke />
	<div class="smallspacer" />
    <img src="code.png" height=100 alt="code icon">
	<h1>Danil Timofeev</h1>
	<h2>I am a student at Innopolis and I love programming and design.</h2>
    <div class="smallspacer" />
	<a href="/projects">
		<button class="firstbutton">Read More</button>
	</a>
	<div class="spacer" />
</section>

<style>
    h1 {
        color: var(--pure-white);
    }
	section {
		margin-top: 60px;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}
	.spacer {
		margin: 60px;
	}
    .smallspacer {
		margin: 16px;
	}

	h2 {
		text-align: center;
		font-size: 18pt;
	}
	.firstbutton {
		font-family: 'Source Code Pro';
		border: none;
		margin: 0 auto;
		display: block;
		border-radius: 25px;
		padding: 15px 30px;
		font-size: 150%;
		background: #0d79de;
		cursor: pointer;
	}

	.firstbutton:hover {
		background: #0d79de;
		color: #eee;
	}

	.firstbutton:active {
		background: #0d79de66;
	}
</style>
