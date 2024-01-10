<script lang="ts">
	var apiURL = 'https://v2.jokeapi.dev/joke/Programming?type=single';

	interface jokeJSON {
		error: string;
		category: string;
		type: string;
		joke: string;
		flags: Map<string, boolean>;
		id: number;
		safe: string;
		lang: string;
	}

	let jokeText: string;

	async function getData(): Promise<void> {
		var response = await (await fetch(apiURL)).json();
		const responseData: jokeJSON = response;
		jokeText = responseData.joke;
	}

	getData();
</script>

<div class="joke">
	<h3>Joke of the day:</h3>
	<p>{jokeText}</p>
</div>

<style>
	h3 {
		color: #eee;
		text-align: center;
	}
	p {
		text-align: center;
	}
</style>
