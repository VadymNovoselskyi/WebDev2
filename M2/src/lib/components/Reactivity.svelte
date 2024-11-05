<script>
    let count = 0;
    let square = 0;
    $: square = count**2;
</script>
 
<h2>Exempel på reaktivitet i SvelteKit</h2>

<fieldset>
    <legend>Counter</legend>
    <button on:click={() => count--}>-</button>
    <output>{count}</output>
    <button on:click={() => count++}>+</button>
</fieldset>

<fieldset>
    <legend>Squarare</legend>
    <output>{square}</output>
</fieldset> 
 
<style lang="scss">
    output {
        font-weight: bold;
        margin: 0.5rem;
    }

    button {
        padding: 0 0.5rem;
        margin: 0.5rem;
    }
</style>