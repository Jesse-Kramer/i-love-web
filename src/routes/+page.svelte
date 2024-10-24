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
    <a href="/projects" slot="header-left">Projects</a>
    <a href="/" slot="header-main">About me</a>
    <a href="/contact" slot="header-right">Contact</a>
</Header>

<main>
    <section>
        <p>
            <span>I create</span>
            <span>cool stuff</span>
            <span>with new</span>
            <span>Technique's</span>
        </p>
    </section>

    <Carousel/>

    <section>
        <ul class="qoutes">
            <li>
                <span>CREATIVITY HAS</span>
                <span>NO</span>
                <span>LIMITS</span>
            </li>
            <li>
                <span>BUILD</span>
                <span>YOUR</span>
                <span>DREAMS</span>
            </li>
            <li>
                <span>LET'S</span>
                <span>WORK</span>
                <span>TOGETHER</span>
            </li>
        </ul>
    </section>
    
</main>

<style>
</style>