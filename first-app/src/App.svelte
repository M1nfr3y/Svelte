<script>
	let name = 'Alessio';
	let age = 30;

	$: upperCaseName = name.toUpperCase();

	$: console.log(upperCaseName);

	$: if(name === 'Silvia'){
		age = 26
	}

	function incrementAge() {
		age += 1;
	}

	function changeName() {
		name = 'Silvia'
	}
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {upperCaseName}, my age is {age}!</h1>
<button on:click="{incrementAge}">Change Age</button>
<button on:click={changeName}>Change Name</button>
