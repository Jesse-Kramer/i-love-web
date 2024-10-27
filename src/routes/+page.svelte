<script>
    import Header from './../components/header.svelte';
    import Carousel from './../components/carousel.svelte';

      // View-transitions
    import ViewTransition  from './../lib/ViewTransition.svelte';
</script>

<ViewTransition>
    <Header>
        <a href="/playground" slot="header-left">Playground</a>
        <a href="/" slot="header-main">About me</a>
        <a href="/contact" slot="header-right">Contact</a>
    </Header>
    
    <main>
        <section class="page-intro">
            <p>I create</p>
            <p>Cool stuff</p>
            <p>With new</p>
            <p>Techniques</p>
        </section>
    
        <Carousel/>
    
        <section class="qoutes-section">
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
    
        <section class="links-section">
            <a href="/playground">My projects</a>
            <a href="/contact">Contact me</a>
        </section>
    
    </main>
</ViewTransition>

<style>
</style>