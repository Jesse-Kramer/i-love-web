<header>
    <nav>
        <ul>
            <li><slot name="header-left"/></li>
            <li><h1><slot name="header-main"/></h1></li>
            <li><slot name="header-right"/></li>
        </ul>
    </nav>
    <hr>
</header>

<style>
header {
    font-size: 10px;

    --header-main: 10em;
    --header-secondary: 5em;

    margin: 1.5em 0 1.5em 0;
}

nav {
    margin-bottom: 1.5em;
}
    
ul {
    display: flex;
    flex-wrap: wrap;
    align-content: center;
    align-items: center;
    justify-content: space-evenly;
}

li {
    text-transform: uppercase;
    font-style: italic;
    font-weight: 300;
}

li:nth-of-type(1), li:nth-of-type(3) {
    font-size: var(--header-secondary);
}

li:nth-of-type(2) {
    font-size: var(--header-main);
}

@media screen and (max-width: 1300px) {
    header {
        --header-main: 2.5em;
        --header-secondary: 1.25em;
    }
}
</style>