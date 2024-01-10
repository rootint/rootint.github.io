<script lang="ts">
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
</script>

<Header />

<main>
	<slot />
</main>

<div class="footer">
	<a href="https://github.com/rootint/">
		<img src="github_icon.png" height="30px" width="30px" alt="github-link" /></a
	>
	<a href="https://t.me/RND_RandoM">
		<img src="telegram_icon.svg" height="30px" width="30px" alt="telegram-link" /></a
	>
</div>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}

	.footer {
        /* bottom: 0; */
		width: 100%;
		overflow: hidden;
		background-color: #222;
		padding: 20px;
	}
</style>
