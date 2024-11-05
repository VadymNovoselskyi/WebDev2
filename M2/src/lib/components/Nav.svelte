<script>
    import { page } from '$app/stores';
    let show = false;
 </script> 

<nav>
    <button on:click={() => show = !show}>
        <img src="/btn-menu.svg" alt="menu btn" height="25" />
    </button>
    <ul on:click={() => show = false} class:show>
        <li><a href="/" class:active={$page.url.pathname === "/"}>Hem</a></li>
        <li><a href="/course" class:active={$page.url.pathname === "/course"}>Kurs</a></li>
        <li><a href="/about" class:active={$page.url.pathname === "/about"}>Om</a></li>
        <li><a href="/reactivity" class:active={$page.url.pathname === "/reactivity"}>Reactivity</a></li>
    </ul>
</nav>

<style lang="scss">
    nav {
        display: flex;
        color: #e2e3db;
        font-size: medium;
        justify-content: end;
        margin-right: var(--margin-l);
        font-size: medium;
        z-index: 10;
        button {
            border: 0;
            background: transparent;
            display: none;
            padding: 0;
        }
        ul {
            list-style-type: none;
            overflow: hidden;
            background-color: #333;
            display: flex;
            z-index: 100;
            li {
                background-color: #333;
                color: #e2e3db;

                a {
                    display: block;
                    text-align: center;
                    padding: 0.8rem 1.6rem;
                    text-decoration: none;
                    font-weight: 600;
                    margin: 0;
                    color: inherit;

                    &.active {
                        background-color: #ff3e00;
                    }
                    &:hover:not(.active) {
                        background-color: #111;
                        color: #fff;
                    }
                }
            }
        }
    }

    @media only screen and (max-width: 768px) {
        nav {
            margin-right: var(--margin-s);
            button {
                display: inline;
                cursor: pointer;
            }
            ul {
                display: none;
                position: absolute;
                top: 4.5rem;
                right: 0.5rem;
                width: 50%;
                li {
                    display: block;
                }
            }
        }
        .show {
            display: block !important;
        }
    }

    @media only screen and (max-width: 420px) {
        nav {
            ul {
                width: 60%;
            }
        }
    }
</style>
