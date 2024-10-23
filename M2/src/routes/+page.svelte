<script>
    let hide = false;
</script>

<svelte:head>
    <title>Main</title>
</svelte:head>

<h1>This one is main!</h1>
<h2>Hello world</h2>

<div><p>Hej</p></div>
<section><p>på dig</p></section>

<br> <br> <br>
<button on:click={() => hide = !hide}>Click</button>
<h1 class:hide = {hide}>Make me invisible!</h1>

<style>
    h1 {
        color: red;
    }
    div p {
        color: blue;
    }
</style>