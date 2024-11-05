<script>
    import Name from "$lib/components/Name.svelte";
    import Reactivity from "$lib/components/Reactivity.svelte";
    import Keyboard from '$lib/components/Keyboard.svelte';

    let data = ''

    let display = "";
    function updateDisplay(e){
        let val = e.target.value;
        if(val === "ac"){
            display = "";
        }else if(val === "c"){
            display = display.slice(0, -1);
        }else if(Number(val) >= 0 && Number(val) <10 ){
            display += val;
        }
    }
</script>

<svelte:head>
    <title>Reactivity</title>
</svelte:head>


<main>
    <h1>Reactivity</h1>

    <fieldset>     
        <legend>Namn med input</legend>
        <Name/>
        <Name bind:name = {data} />
        <p>Namn: {data}</p>
    </fieldset>

    <Reactivity />
    <br><br>

    <fieldset>
        <legend>KeyBoard</legend>
        <input type="text" value={display} disabled />
        <Keyboard on:click={updateDisplay}/>
    </fieldset>     
</main>

<style lang="scss">
    fieldset {
        margin: 2rem 0;
    }
</style>