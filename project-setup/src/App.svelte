<script>
	let name = "Alessio";
	let age = 27;

	function increment(){
		age += 1
	}
</script>

<h1>Hello {name}, la mia età è {age}!</h1>
<button on:click={increment}>Change Age</button>

<style>
	h1 {
		color: purple;
	}
</style>
