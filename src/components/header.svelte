<header>
    <nav>
        <ul>
            <li><a href="#">Projects</a></li>
            <li><a href="#">About me</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>
    <hr>
</header>

<style>
header{
    font-size: 10px;

    --header-main: 10em;
    --header-secondary: 5em;

    margin: 1.5em 0 1.5em 0;
}

nav{
    margin-bottom: 1.5em;
}

a{
    color: inherit;
    font-size: inherit;
    text-decoration: inherit;
}
    
ul{
    display: flex;
    flex-wrap: wrap;
    align-content: center;
    align-items: center;
    justify-content: space-evenly;
}

li{
    text-transform: uppercase;
    font-style: italic;
    font-weight: 200;
}

li{
    font-size: var(--header-secondary);
}
</style>