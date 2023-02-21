<script>
	import ContactCard from "./ContactCard.svelte";

	let jobTitle;
	let userImage;
	let description = "pene";
	let name = "Alessio";
	let age = 30;

	$: upperCaseName = name.toUpperCase();

	$: console.log(upperCaseName);

	$: if (name === "Silvia") {
		age = 26;
	}

	function incrementAge() {
		age += 1;
	}

	function changeName() {
		name = "Silvia";
	}

	function nameInput(event) {
		const inputName = event.target.value;
		name = inputName;
	}
</script>

<h1>Hello {upperCaseName}, my age is {age}!</h1>
<button on:click={incrementAge}>Change Age</button>
<!-- <button on:click={changeName}>Change Name</button> -->
<!-- <input type="text" value="{name}" on:input={nameInput}> -->
<input type="text" bind:value={name} />
<input type="text" bind:value={jobTitle} />
<input type="text" bind:value={userImage} />
<textarea rows="3" bind:value={description} />

<ContactCard userName={name} {description} {jobTitle} {userImage} />

<style>
	h1 {
		color: purple;
	}
</style>
