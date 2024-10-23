<header>
    <nav>
        <ul>
            <li><slot name="header-left"/></li>
            <li><slot name="header-main"/></li>
            <li><slot name="header-right"/></li>
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

li:nth-of-type(1), li:nth-of-type(3){
    font-size: var(--header-secondary);
}

li:nth-of-type(2){
    font-size: var(--header-main);
}
</style>