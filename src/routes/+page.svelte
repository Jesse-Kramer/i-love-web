<script>
    import Header from './../components/header.svelte';
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

</main>

<style>
</style>