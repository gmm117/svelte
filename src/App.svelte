<script>
	export let name;
	let count = 1;
	$: double = count * 2;
</script>

<main>
	<h1 id="root">Hello {name}!</h1>
	<h1> count : {double}</h1>
	<button on:click={() => count += 1}>increase</button>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	#root {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>