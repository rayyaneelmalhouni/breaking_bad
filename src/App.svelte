<script>
	import Search from './components/Search.svelte';
	import Show from './components/Show.svelte';
	let names;
	async function search() {
		const info = await fetch("https://breakingbadapi.com/api/characters");
		const data = await info.json();
		console.log(data)
		return data;
	}
	let data = search()
	
	function name_generator(data) {
		let names = [];
		for (let i = 0; i <data.length; i++) {
		    		names.push(data[i].name)
		}
		return names;
		
	}
	
	
	// window.onload = search();
	// console.log(names)
	
</script>

<main >
	<div class="container">
		<div class="titles">
			<h1>Breaking Bad</h1>
		<h2>Actor Searcher</h2>
		</div>
		
	<Search />
	<Show />
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