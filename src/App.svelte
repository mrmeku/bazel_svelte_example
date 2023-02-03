<script>
	import Component from "./Component.svelte";

	let name = "world";
</script>

<div>
	<h1 class="header">Hello {name}!</h1>
	<label>
		Name: <input bind:value={name} />
	</label>
	<hr />
	<Component {name} />
</div>

<style>
	.header {
		font-family: sans-serif;
	}
</style>
