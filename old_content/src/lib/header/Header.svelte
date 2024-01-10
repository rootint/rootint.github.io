<header>
	<div class="navbar">
		<a href="#home"><img src="favicon.png" height="25" alt="icon" /></a>
		<div class="navbar-right">
			<a sveltekit:prefetch href="/">Home</a>
			<a sveltekit:prefetch href="/projects">Projects</a>
			<a sveltekit:prefetch href="/about">About Me</a>
		</div>
	</div>  
</header>

<style>
	.navbar {
		overflow: hidden;
		background-color: #222;
		position: fixed;
		top: 0;
		padding: 0;
		width: 100%;
		font-size: 120%;
	}

	.navbar a {
		float: left;
		display: block;
		color: #0d79de;
		text-align: center;
		padding: 18px;
		text-decoration: none;
	}

	.navbar a:hover {
		background: #0d79de;
		color: black;
	}

	.navbar-right {
		float: right;
	}
	header {
		display: flex;
		justify-content: space-between;
	}
    
	a:hover {
		color: var(--accent-color);
	}
</style>
