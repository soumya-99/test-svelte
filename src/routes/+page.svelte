<script lang="ts">
	let count: number = 0
    console.log('Pagee');
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


<style>
    .container {
        display: flex;
        align-items: center;
        justify-content: space-around;
        height: 100vh;
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
</style>
