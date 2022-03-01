<script>
	import Search from './components/Search.svelte';
	import Show from './components/Show.svelte';
	async function search() {
		const info = await fetch("https://breakingbadapi.com/api/characters");
		const data = await info.json();
		console.log(data);
	}
</script>

<main>
	<div class="container">
		<div class="titles">
			<h1>Breaking Bad</h1>
		<h2>Actor Searcher</h2>
		</div>
		
	<Search />
	<Show />
	<button on:click={search}>Click</button>
	</div>
	
</main>

<style>
	.container {
		width: 60%;
		border: 1px solid #333;
		border-radius: 15px;
		
		margin: 0 auto;
		padding: 10px;
	}
	.titles {
		margin-bottom: 40px;
		text-align: center;
	}
	h1 {
		font-size: 36px;
		color:#00008b;
	}
	h2 {
		color: #333;
		font-size: 24px;
	}

</style>