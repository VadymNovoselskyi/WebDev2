<script>
    let num = 0;
    let square = 0;

    function inc() {
        num++;
    }
    function dec() {
        num--;
    }

    $: square = num**2;
</script>

<fieldset>
    <label>Calc</label>
    <button on:click={dec}>dec</button>
    <output>{num}</output>
    <button on:click={inc}>inc</button>
</fieldset>
<br><br>
<fieldset>
    <label>Square</label>
    <output>{square}</output>
</fieldset>