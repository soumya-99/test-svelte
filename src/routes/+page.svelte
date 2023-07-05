<script lang="ts">
	let count: number = 0
	console.log("Pagee")

	let inputText: string = ""
	let inputColor: string = "#aaa"
	let todos: string[] = []
</script>

<svelte:head>
	<title>Page</title>
	<meta name="description" content="Page description" />
</svelte:head>

<div style="text-align: center; font-family: google sans;">
	<h1>Just a Counter to Test Svelte</h1>
	<hr />
</div>

<div class="container">
	<button class="btn" on:click={() => count--}> Remove (-) </button>

	<div class="count">{count}</div>

	<button class="btn btn-1" on:click={() => count++}> Add (+) </button>
</div>

<div class="todo">
	<input type="text" placeholder="Type something" bind:value={inputText} />
	<input type="color" bind:value={inputColor} />

	<button
		class="btn"
		on:click={() => {
			todos = [...todos, inputText]
			inputText = ""
		}}
	>
		Add Todo
	</button>
</div>

<div class="view_todo">
	<ul>
		{#each todos as todo}
			<li style="color: {inputColor}">{todo}</li>
		{/each}
	</ul>
</div>

<style>
	.container {
		display: flex;
		align-items: center;
		justify-content: space-around;
	}

	.btn {
		background-color: #ff3a17;
		border: none;
		border-radius: 15px;
		color: white;
		padding: 25px 35px;
		text-align: center;
		text-decoration: none;
		cursor: pointer;
		display: inline-block;
		font-family: google sans;
		font-size: 20px;
		font-weight: bold;
	}

	.btn-1 {
		background-color: #16d804;
	}

	.count {
		font-size: 60px;
		font-family: google sans;
		color: #227c16;
	}

	.todo {
		display: flex;
		justify-content: space-around;
		align-items: center;
		margin: 20px;
	}

	.view_todo {
		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>
