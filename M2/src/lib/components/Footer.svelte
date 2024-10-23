<footer>
    <h1>FOOTER TEST</h1>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
        <li>5</li>
    </ul>
</footer>

<style>
    footer {
        display: grid;
        background-color: #222222;
        width: 100vw;
        height: 20vh;
        color: #bada55;
    }
    h1 {
        padding: 1rem;
    }
    ul {
        display: grid;
        grid-template-columns: repeat(5, 1fr);
        justify-items: center;
        align-items: center;
    }
    li {
        list-style: none;
    }
</style>