<section>
    <button value="7" on:click>7</button>
    <button value="8" on:click>8</button>
    <button value="9" on:click>9</button>

    <button value="4" on:click>4</button>
    <button value="5" on:click>5</button>
    <button value="6" on:click>6</button>

    <button value="1" on:click>1</button>
    <button value="2" on:click>2</button>
    <button value="3" on:click>3</button>

    <button value="ac" on:click>AC</button>
    <button value="0" on:click>0</button>
    <button value="c" on:click>⇦</button>
</section>

<style lang="scss">
    section {
        display: grid;
        grid-template-rows: repeat(4, 1fr);
        grid-template-columns: repeat(3, 5rem);

        button {
            font-size: 1.5rem;
            font-weight: bold;
            width: 5rem;
            height: 5rem;
        }
    }
</style>
