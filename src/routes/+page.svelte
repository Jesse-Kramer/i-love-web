<script>
    import Header from './../components/header.svelte';
    import Carousel from './../components/carousel.svelte';
    import { onNavigate } from '$app/navigation';

    onNavigate((navigation) => {
        if (!document.startViewTransition) return;

        return new Promise((resolve) => {
            document.startViewTransition(async () => {
                resolve();
                await navigation.complete;
            });
        });
    });
</script>

<Header>
    <a href="/playground" slot="header-left">Playground</a>
    <a href="/" slot="header-main">About me</a>
    <a href="/contact" slot="header-right">Contact</a>
</Header>

<main>
    <section class="entry">
        <p>I create</p>
        <p>Cool stuff</p>
        <p>With new</p>
        <p>Techniques</p>
    </section>

    <Carousel/>

    <section class="qoutes">
        <ul>
            <li>
                <p>Creativity</p>
                <p>has</p>
                <p>No</p>
                <p>limit</p>
            </li>
            <li>
                <p>Build</p>
                <p>your</p>
                <p>dreams</p>
            </li>
        </ul>
    </section>

    <section class="links">
        <a href="/playground">My projects</a>
        <a href="/contact">Contact me</a>
    </section>

    <section class="mobile message-app">
        <p class="incoming">Bro, I thought they taught to build mobile first. 😂</p>
        <p class="outgoing">Uhm, yeah I did desktop first 💀, but I'm going to build the mobile version soon!📱</p>
        <p class="status">Read</p>
    </section>
    
</main>

<style>
</style>